<div style="font-size: 2em;font-weight:bold">Mildred is retiring!</div>
<img src="assets/bw.jpg" style="width:20vw;border-radius:2em"/>
<div>After 60 years of service.</a>
<div>Please sign her farewell card <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ">here</a>


<h1>How to run?</h1>
<ol>
    <li>Run <code>get_movie_time.py |input file here|</code> and receive this week's schedule</li>
    <li>That's it!</li>
</ol>

<h1>How to change hours?</h1>
If you need to change hours for this week, update them in the <code>hours.ini</code> file.

<h1>Support</h1>
Any issues, please contact script creator <a href="https://www.youtube.com/watch?v=p85xwZ_OLX0">here</a>

<hr>

<h1>Dev notes:</h1>
<h1>Specs</h1>
<ul>
    <li>Operation hours</li>
        <ul>
            <li>Monday - Thursday, 8:00AM - 11:00PM</li>
            <li>Friday - Sunday, 10:30AM - 11:30PM</li>
            <li>Make them parametrized, subject to change.</li>
        </ul>
    <li>Overhead</li>
        <ul>
            <li>Beginning of day: 1 hour setup before any movie.</li>
            <li>35 mins between movies.</li>
            <li>Movie cannot end after theatre closing time, which is midnight</li>
            <li>Movie cannot start after theatre hours. I.e., Between theatre hours end and closing time.</li>
        </ul>
    <li>Prioritize movies schedule later in the day</li>
    <li>Have rounded times. E.g., 4:00PM, 2:35PM. Not 6:32PM</li>
    <li>Assume movie theatre has no limit of number of screens.</li>
    <li>Soft performance spec: Must return answer within reasonable time (e.g., less than 5 sec)</li>
    <li>Input is CSV</li>
        <ul>
            <li>No commans expected in data payloads.</li>
            <li>No limit on size.</li>
            <li>Assume char set UTF-8.</li>
        </ul>
    <li>Output</li>
        <ul>
            <li>Show the date in format <code>Day of week name|MM|DD|YYYY|</code></li>
            <li>Show the movie name, rating, and duration in 24 hour "military" time format</li>
            <li>Show the available show times and end time for every movie</li>
        </ul>
        
            

</ul>

<h1>Test data</h1>
<ul>
    <li><code>happy_path.csv</code> "Happy path" data</li>
    <li><code>error_handle.csv</code> Possible valid CSV but contains invalid data for our application</li>
        <ul>
            <li>Special chars</li>
            <li>Empty value</li>
            <li>Invalid year</li>
            <li>Invalid runtime</li>
            <li>Duplicate entries</li>
            <li>UTF-8 chars</li>
        </ul>
    <li><code>line_break.csv</code>Mistaken line feeds</li>
    <li><code>duplicate.csv</code>Duplicate movies</li>
    <li><code>not_a_csv.csv</code> A regular text file</li>
    <li><code>empty_file.csv</code> An empty file</li>
    <li><code>stress.csv</code> A really long file</li>
</ul>
