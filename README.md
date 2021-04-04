# How you know your Free or Open Source Software Project is doomed to FAIL

**FOSS-POF (Free or Open Source Software Points Of Fail)** is a simple app to self-analyse your Open Source Project and help you take the necessary measures to prevent it from being doomed to fail.

Through a list of points that you can check according to the characteristics of your Open Source project, you will obtain a result that indicates whether your software is doomed to fail.

Those points were originally written by [Tom 'spot' Callaway](http://fedoraproject.org/wiki/User:Spot) and are used here under the MIT license. The work [How you know your Free or Open Source Software Project is doomed to FAIL (or at least, held back from success)](http://spot.livejournal.com/308370.html) originally appeared on 2009-05-29 at this URL: http://spot.livejournal.com/308370.html

> This was inspired by Spot's initial efforts to look at [Chromium](http://code.google.com/chromium/), but these are just some of the red flags he generally has observed over the years, now written down.

> There are obvious exceptions, such as the Linux kernel.
Generally these exceptions work because they started out small and the community and code grew together. Large complexity requires a large community. Starting a new project with lots of complexity makes it exceedingly hard to build up a community.

## Building and Running FOSS-POF Locally

1. Clone the source code

```
git clone https://github.com/s3rrot/foss-pof.git
```

2. Install development dependencies

```
yarn install
```

3. Run a local development server (including hot-reload)

```
yarn serve
```

FOSS-POF is now running, and can be accessed by pointing a web browser at http://localhost:8080/

## License

The FOSS-POF project is available under the [MIT License](https://opensource.org/licenses/MIT).

## Reference
[How to tell if a FLOSS project is doomed to FAIL](https://www.theopensourceway.org/wiki/How_to_tell_if_a_FLOSS_project_is_doomed_to_FAIL#Source_Control) [CC BY SA 3.0](http://creativecommons.org/licenses/by-sa/3.0/) license