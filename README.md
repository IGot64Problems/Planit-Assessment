# Planit-Assessment

Additional Questions

1.  You are given a requirement which states "The system should scale to 2000 users"

Further questions.

a.  2000 users performing 1 "search" per minute?

b.  On average, how many times is the suggestion API invoked?

c.  Does the typical user do just one search, from the home page?  Or do some refine the search further once the results are displayed?  (Will there be additional calls to the suggestion API and perhaps a second search).  What percentage of users refine/repeat a search?  50%?

d.  Latency expectations.  For example, home screen is downloaded in 1 second, suggestion API under 0.2 seconds, results downloaded in under 2 seconds.

2.  Rewrite the requirement above so that it is testable and more descriptive

The system should scale to 2000 users performing a complete search every minute.  On average, each search entry invokes 3(?) requests to the suggestion API.  50% of the users will refine the search results and repeat the search.  i.e. the search box at the top of the results page will be used and the home page will not be reloaded.  The following latencies are expected:

a. Home page downloads in 1 second
b. Suggestion API takes less than 0.2 seconds to respond
c. Search results are downloaded in under 2 seconds.

Note, download times do not include time for web browser to render results.

3.  What other factors would need to be considered for a performance testing engagement?

a.  What type of testing is required - load testing, stress testing, break point, long runs, etc.
b.  As mentioned, expected latencies.  i.e. for a load test, what response times can be considered a "fail"
c.  Environment monitoring - monitoring CPU, memory, disk usage, etc. during a test
