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
* your server should receive data that looks something like this:
```
{
  context: {
    page: {
      path: '/example/index.html',
      referrer: 'http://127.0.0.1:5501/example/index.html',
      search: '',
      title: 'Document',
      url: 'http://127.0.0.1:5501/example/index.html'
    },
    userAgent: 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/102.0.0.0 Safari/537.36',
    library: { name: 'analytics.js', version: '2.11.0' }
  },
  integrations: {},
  properties: {
    path: '/example/index.html',
    referrer: 'http://127.0.0.1:5501/example/index.html',
    search: '',
    title: 'Document',
    url: 'http://127.0.0.1:5501/example/index.html'
  },
  anonymousId: '960a3cff-fb2b-42e9-88b1-ba441eb43109',
  timestamp: '2022-06-15T18:03:41.598Z',
  type: 'page',
  userId: null,
  messageId: '39151a25-f4eb-4272-97ca-9005ba8275ea',
    title: 'W3A Example',
    url: 'http://127.0.0.1:5501/example/index.html'
  },
  anonymousId: '960a3cff-fb2b-42e9-88b1-ba441eb43109',
  timestamp: '2022-06-15T18:04:15.468Z',
  type: 'page',
  userId: null,
  messageId: '4ce44431-90fd-450a-a22f-3cd64e41be3c',
  sentAt: '2022-06-15T18:04:15.470Z'
}
```
* for more events check https://segment.com/docs/connections/sources/catalog/libraries/website/javascript/#basic-tracking-methods
