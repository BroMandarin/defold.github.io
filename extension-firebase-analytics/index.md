---
layout: manual
language: en
github: https://github.com/defold/extension-firebase-analytics
title: Defold Firebase Analytics documentation
brief: This manual covers how to setup and use Firebase Analytics in Defold.
---

# Defold Firebase Analytics documentation

This extension allows you to interact with Firebase Analytics in a uniform way for games on iOS and Android.


## Installation
To use this library in your Defold project, add the following URL to your `game.project` dependencies:

* [https://github.com/defold/extension-firebase/archive/master.zip](https://github.com/defold/extension-firebase/archive/master.zip)
* [https://github.com/defold/extension-firebase-analytics/archive/master.zip](https://github.com/defold/extension-firebase-analytics/archive/master.zip)

We recommend using a link to a zip file of a [specific release](https://github.com/defold/extension-firebase-analytics/releases).


## Setup
Follow the [main setup guide for integration of Firebase in Defold](https://www.defold.com/extension-firebase).



## Usage

```lua
function init(self)
	-- use firebase only if it is supported on the current platform
    if not firebase then
        return
    end

	-- initialise firebase and check that it was successful
    local ok, err = firebase.init()
    if not ok then
        print(err)
        return
    end

	-- initialise analytics
	firebase.analytics.init(function(self, ok, err)
		if not ok then
			print(err)
			return
		end

		-- log data
		firebase.analytics.set_screen("myscreen", "collection")
		firebase.analytics.log_string("character", "storm trooper")
		firebase.analytics.log_int("kills", 152)
		firebase.analytics.log_number("speed", 1.15)
		local t = {
			number = math.random(1,100),
			boolean = true,
			string = "some_string"
		}
		firebase.analytics.log_table("stats", t)
	end)
end
```

## Source code

The source code is available on [GitHub](https://github.com/defold/extension-firebase-analytics)


## API reference
[API Reference](/extension-firebase-analytics/api)