### Prerequisite:
* A server having POST route for http://localhost:3000/api/v1/view_event

NOTE: Checkout the example in example/index.html once to get a better understanding of code snippet below.

### Steps for running code
* clone this repo
* create a html file
* include analytics.js in your body tag
* include this code snippet in script tags
 ```
     <script>
        analytics.initialize({
            "W3A" : {
                "api_key" : ""
            }
        })
        analytics.page()
    </script>
 ```
