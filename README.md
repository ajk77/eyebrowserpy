# EyeBrowserPy

Eye (gaze) tracking in your browser, plus area of interest analysis code. 

## Getting Started

This package provides code for adding eye-tracking to LEMRinterface (https://github.com/ajk77/LEMRinterface). It is intendend for demonstrative purposes only. 

### Prerequisites

A remote eye-tracking device and its driver files. I used a Tobii gaming device (https://gaming.tobii.com/). <br />
The python wrapper pachage gazesdk (https://github.com/balancana/gazesdk). 

#### Note

gazesdk requires you to put TobiiGazeCore32.dll into your /python/lib/site-packages/ directory. 

### Installing

Download eyebrowser.py, gazesdk.py, and the eye tracking devices driver files. <br />
Place the dll file in the /python/lib/site-packages/ directory.<br />
Test the code by calling eyebrowserpy.start_eye_stream().

### Deployment

Annotate your web interface as follows: <br />
* Each container (e.g. a div) must have a known id or be part of a class so that they can be identified via jQuery.
* Container locations are returned as as a comma separated list of container_id, top edge, left edge, bottom edge, right edge, next_container_id, ...
* Optional, containers are only returned if they are displayed within the bounds of a larger container. This is recommended if many containers are scrolled off screen.
* For static containers that contain a scroll bar, the scroll position can be returned instead. 
* The browser must be full screen for pixel locations to be accurately mapped to the output stream of the eye tracking device.

#### Note

The analysis code assumes the browser is run in full screen mode on a 1920 x 1080 resolution monitor. On some browsers, smooth scrolling will need to be turned off.  Responsive html is not
currently support.

## Versioning

Version 2.1. For the versions available, see https://github.com/ajk77/EyeBrowserPy

## Authors

* Andrew J King - Doctoral Candidate (at time of creation)
	* Website (https://www.andrewjking.com/)
	* Twitter (https://twitter.com/andrewsjourney)
* Shyam Visweswaran - Principal Investigator
	* Website (http://www.thevislab.com/)
	* Twitter (https://twitter.com/Shyam_Vis)
* Gregory F Cooper - Doctoral Advisor


## Impact
This interface has been used in the following studies:

* King AJ, Cooper GF, Clermont G, Hochheiser H, Hauskrecht M, Sittig DF, Visweswaran S. Leveraging Eye Tracking to Prioritize Relevant Medical Record Data: Comparative Machine Learning Study. J Med Internet Res 2020;22(4):e15876. (https://www.jmir.org/2020/4/e15876/)
* King AJ, Hochheiser H, Visweswaran S, Clermont G, Cooper GF. Eye-tracking for clinical decision support: A method to capture automatically what physicians are viewing in the EMR. AMIA Joint Summits. 2017 Mar 27-30; San Francisco, California p 512-521. [Best Student Paper] (https://www.ncbi.nlm.nih.gov/pubmed/28815151)

## License

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.

## Acknowledgments

* Harry Hochheiser
	* Twitter (https://twitter.com/hshoch)
* Gilles Clermont
* Milos Hauskrecht 
