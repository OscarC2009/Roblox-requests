# Roblox-requests
Roblox client-sided examples of how to send information to a URL, and also how to recieve.

Post to a server (METHOD: POST): 

```lua
local HttpService = game:GetService("HttpService")

-- URL to send the POST request to
local url = "https://www.example.com/"

local function sendGetRequest(url)
    local success, response = pcall(function()
        -- Make the GET request
        return http_request({
            Url = url,
            Method = 'POST',
            Headers = {
                ['Content-Type'] = 'application/json'
            },
        })
    end)

    if success then
        print("Response received:")
        print(response.Body) 
    else
        warn("Request failed:", response)
    end
end

sendGetRequest(url)
```

Recieve from a server (METHOD: GET)

```lua
local HttpService = game:GetService("HttpService")

-- URL to send the GET request to
local url = "https://www.example.com/"

local function sendGetRequest(url)
    local success, response = pcall(function()
        -- Make the GET request
        return http_request({
            Url = url,
            Method = 'GET',
            Headers = {
                ['Content-Type'] = 'application/json'
            },
        })
    end)

    if success then
        print("Response received:")
        print(response.Body) 
    else
        warn("Request failed:", response)
    end
end

sendGetRequest(url)
```

Tested on: [Celery](https://celery.zip/)
