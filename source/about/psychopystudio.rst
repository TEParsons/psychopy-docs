.. _psychopystudio:

PsychoPy Studio
=====================================

In early 2026 we released a new version of the|PsychoPy| app, PsychoPy studio. You can read more about why PsychoPy studio was created and what we hope it will offer for the future `in this blog post <https://blog.psychopy.org/psychopy/psychopy_studio/>`_. 

In April, we hosted a webinar to introduce PsychoPy studio to the world, you can watch the webinar below and read the Q & A from attendees. We really hope that you will like PsychoPy studio - please download it and try it (it can be installed alongside your standalone release) please share your feedback via `the PsychoPy forum <https://discourse.psychopy.org/>`_.


`Watch our launch webinar on YouTube <https://www.youtube.com/watch?v=kwkiWzwJNDs>`_.


Q&A from Webinar Attendees
--------------------------

**"Does Psychopy have newer articles or releases to cite than those listed here, or should we still go with these?
https://psychopy.readthedocs.io/en/stable/about/index.html"**

    No not yet - but hopefully soon!

**Many here rely on Psychopy’s old photometer support and automated gamma measurement/correction tool in Monitor Center.  Just a minor request to please keep that functionality if possible!**

    This is absolutely our intention, yes! There's a few bugs in the current release that we're hoping to fix soon, but the intention is very much to keep that functionality.

**Nice to see the presentation is on Linux :-). Two Qs: 1) Any official documentation about installing to Linux?  2) A typical error on Linux installations was the (in)ability to upload/sync to Pavlovia. Is this still the case?**

    1) On the download page (psychopy.org/download), there's tabs for each OS. For Standalone there's instructions for the old method, for Studio it's just a downloadable .AppImage file (installing will depend on your distro, I used Gear Lever for my Bazzite GNOME setup)
    2) I've been syncing to Pavlovia from Studio on Linux and generally found it much the same as on Windows/Mac :)

**Will the QoL updates shown also be added to the regular version?**

    If you mean things like drag and drop of components and loops, then no, since it is the way Studio has been written that makes these easy to implement.

**Does PsychoPy Studio support adding Additional resources (e.g., Webgazer) like before?**

    Yes! For the webgazer example specifically - this is currently implemented with javascript code components in a Builder experiment. Since you can still use code components (including JavaScript code components) in Studio - then this means you should be able to interact with external packages including webgazer.js in the same way.

**For teaching in the Autumn 26 would you recommend sticking to Standalone or making a jump? **

    I personally am hoping to be able to switch to Studio for teaching from version 2026.2.0, which should be released  in time for the Autumn.

**I have two question: 1, I am currently collecting data using PsychoPy Standalone, if I switch to psychopy studio now, will it affects the data and creat mismatch between my old data file and new data file? 2. I just installed it (super fast to open!) I notice that there is no separate app/icon for psychopy runner? Sometime, we let the student run the study with only the the Runner so they don't change anything in the experiment, since some of them don't have experience with the software.**

    In preferences you can choose which view opens when you open the app (to select Runner) - but yes we do want to retain runner view for the purpose you describe. 

    There shouldn’t be mismatch between your data files - however we do recommend testing in the same way as you would when moving between standalone releases. Do remember to turn on use version.

**Any  way to test run experiments without having user input? As you can in E-Prime at a silly test speed generating test data?**

    There is a plugin already available called "monkeys" which does this. Try installing it from the Plugins menu.

**Does the studio (browser) version has any implications for controlling local devices (eyetracking, EEG, biopac, etc)**

    The packaged electron app can still communicate with hardware in the same way (it still uses the same python libraries). In future when this is in a webpage this could be difficult because browsers could place limitations on python based functionalities.

**Are there any plans to add some sort of interface to rearrange components within a routine by using drag and drop **

    This is already possible in Studio (but not Standalone) using drag-and-drop!

**We have users that write their entire experiment in a conda environment.  They don’t use any Psychopy GUIs at all.  They just pip install psychopy and write their code.  Should I warn them that this may go away?**

    No. If you don’t use the app GUI at all then `pip install psychopy` will achieve exactly the same in the future as it does now. Actually it should be easier because, without the app being included, there are fewer dependencies, like no need for wxpython.
    It should also be easier to use in a combination - install the Studio app and it will get a venv ready for you to use from other places (in a way that the old standalone python was not)

**Are there any obvious bugs in the current PsychoPy Studio build?**

    If you go to github and look up psychopy-studio repo any pull request that starts with BF reflects a bugfix pull request. Those most important to look out for are: Loading of plugins, monitor center and interacting with pavlovia. but these will be fixed soon.

**I wrote a PsychoPy app that makes it easier to find coordinates of objects on the screen. It helped me develop a page with lots of objects on the page. I can describe in more detail if interested.**

    That sounds interesting. Is it something you could share on the PsychoPy forum https://discourse.psychopy.org/ ?

**Could you please do an introduction to the plugin system and how it may have changed?  Are there new plugin requirements?  Any plugin development resources?**

    We don’t anticipate any real changes around plugins, although the icons can now support vector (svg) files (and that has the advantage we can adapt them more easily at runtime according to the theme)

**Is there a way of converting old experiments into studio version (beyond just running old versions in studio)**

    The file format is exactly the same (.psyexp) so you should be able to simply open your old experiments in Studio. The Studio itself is just a 'wrapper' to interact with the PsychoPy Python library, which hasn't changed.

**Hello I have 2 silly questions: "Do I need to download PsychoPy to use Pavlovia in the browser? When will the Pavlovia app be available for download?"**

    Currently you need to download PsychoPy Studio (or PsychoPy standalone) to write an experiment suitable for running the browser. The plan is that eventually you will be able to write experiments directly in a web version of PsychoPy Studio and won't need to download anything unless you want to run locally. PsychoPy Studio is available to download now. There is also a different "PsychoPy App" which is in development.

**Studio is smooth  as you mentioned and standalone takes a lot of time to open and its slow, I have already developed an experiment in standalone, would it be more easy to replicate the same in the studio by following the same procedure with some minimal changes. And if there is any guide  avilable to use Psychopy studio more conveniently**

    You should be able to open the experiment you've already created in Standalone in Studio and run/edit it from there (although of course if not, let us know via the forum - discourse.psychopy.org!). The interface itself is very similar to the Standalone version so our current docs should hopefully help!

**Is it possible to use the app in a browser on a tablet?**

    Not yet, but this will be coming soon -- hopefully next year.

**I'd appreciate it if you could tell me whether you think there'd be any problem running an experiment programmed using the 2023.2.3. on the latest PsychoPy Studio. I upgraded it once to a 2025 version but my experiment crashed. Though, I don't remember what the error was now. So, I downgraded back to the 2023 version. Everything works great with the 2023.2.3 version for me, I am concerned once I switch to PsychoPy studio, again my experiment will crash.**

    We would suggest giving it a go but duplicate the folder (don’t save over the original folder) - and let us know in the forum! In theory Studio has better use version functionality - so the experiance should be better - but test carefully and please let us know.

**Will future workshops be using PsychoPy Studio for all the demos?**

    Yes! Sometime soon, at least when it doesn’t carry the “Beta” tag anymore (that’s the key to us thinking this is production ready)

**Any changes related to the rendering of fonts in the Studio, especially non-English fonts? I had experienced issues while showing two different fonts in the same routine.**

    There is no changes to this based on Studio - any issues will be due to the python library rather than the studio interface. There have been some recent fixes (which might fix the issue you describe) - but keep us posted on the forum!

**Are you planning to add a kind of layout view to Studio that makes it easier to place components on the screen?**

    YESSS we really would like this - and wx was holding us back - so fingers crossed this should happen at some point.

**Apple warns me that “this version” of Standalone PsychoPy will not open in future versions of MacOS. 1. Is that going to be a problem with Standalone for Mac users “soon” and 2. Will Studio avoid this problem?**

    This should be fine. So far we have been supporting newer chips using an emulator mode in rosetta for mac OS but that is being dropped in the near future. However from this summer we should support native mac sillocon arm chips (2026.2.0 onwards).

**I’m not sure if this is already default behavior during installation in Windows, but if not, it would important to allow Studio installs on a per user account basis (Standalone does this).  We have shared machines where each user has a login.**

    To summarise the live anser: Currently, Studio installs to Program Files (so system-wide and requires admin), but creates its Python environments and saves preferences in a user space. So installing the software itself requires admin, but once installed users will retain their own preferences and shouldn't need admin access to make new Python environments (e.g. when running an experiment set to use an older version). I believe it's possible in Electron to add a choice in the installer whether to install in Program Files or some user space, so I'll look into it for the next major release :) 

**Hi! I am testing the app on Mac. When trying to add a loop, the app displays ‘Loading loops…’ and goes nowhere from here. Is this a bug or am I doing something wrong? Thanks a lot!**

    You might need to wait a bit and reload the app! on first install you will see “Loading Components” and there might be something similar for loops - so give it a little time and re-open and I suspect this should work as expected.

**I just tried to install it on my Uni PC and I need admin to sign in**

    Thanks for the feedback.

**Where are the studio stickers????😬😂**

    VERY important question. We are awaiting our new merch to arrive… very soon…

**Translation to other languages sometimes gets funny but it's a bit difficult to go back to English in the Standalone. Is this something that could be made easier in Studio?**

    Yes! Unfortunately translation didn't quite make it into the release but we've got a new system for label translations ready to go in 2026.2.0 and have been coordinating our volunteer translators getting ready to translate all the new labels Studio adds

**Would like to report that for our uni where we used a cloud computing system for student learning, we just had admin install the standalone version on their end. Students had their own settings and preferences on their own terminals. Not sure about studio but will see**

    Yes, this will be similar for Studio but we’ll need to provide this new option to allowyour admins to configure where the Python environments are stored (to prevent a machine with 50 users having 50+ python installations on it)
