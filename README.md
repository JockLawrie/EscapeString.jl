# EscapeString

[![Build Status](https://travis-ci.org/JockLawrie/EscapeString.jl.svg?branch=master)](https://travis-ci.org/JockLawrie/EscapeString.jl)
[![Coverage Status](http://codecov.io/github/JockLawrie/EscapeString.jl/coverage.svg?branch=master)](http://codecov.io/github/JockLawrie/EscapeString.jl?branch=master)


### Usage
EscapeString provides a single function that escapes a given string according to the given format. The function signature is `escapestring(s::AbstractString, fmt::Symbol)`. For example:
```julia
s  = "<div><b>Hi there 'Sam'!</b></div>"
s2 = escapestring(s, :html_text)
s2 == "&lt;div&gt;&lt;b&gt;Hi there &#39;Sam&#39;!&lt;/b&gt;&lt;/div&gt;"    # true
```

The following formats are currently supported:
- HTML text (`:html_text`)


### Todo
1. Other formats will be added over time on an as-needed basis, such as:
    - HTML attribute
    - URL, also known as percent encoding
    - CSS
    - XML
