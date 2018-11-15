# Scala

Make sure you have Java installed, the instructions are provided [here](/mac-setup/Java/README.html).

    $ brew update
    $ brew install scala
    $ brew install sbt

Update the `~/.sbtconfig` by running the command below. This step is optional.

    $echo 'SBT_OPTS="-XX:+CMSClassUnloadingEnabled -XX:PermSize=256M -XX:MaxPermSize=512M -Xmx2G"' >> ~/.sbtconfig

### Scala Plugin for Eclipse

Scala IDE for Eclipse is best installed (and updated) directly from within Eclipse.

This is done by using `Help → Install New Software...`, add the `Add...` button in the dialog.

Choose a name for the update site (Scala IDE is an obvious choice). Then read the next section to select which version you will install.

**Choosing what version to install**

The list of URLs of the different update sites are available in the download area. The release ones are in the current section. Scala IDE is linked to specific version of Scala, so you have to decide which one you are going to use:

For Scala `2.10`: provides support for projects using Scala 2.10 (any minor version). This is the current version of Scala. Pick this one if you are unsure.

For Scala `2.9`: provides support for projects using Scala 2.9 (any minor version).

The version of Scala used inside Scala IDE cannot be chosen per project. So, if you want to work with a project using different version of Scala (like 2.9.3 and 2.10.1), you need different installation of Scala IDE.

**Finishing installation**

Copy the URL as location and hit OK to validate.

Select Scala IDE for Eclipse from the list of available features.

If you want to install any additional plug-ins (this step is optional), expand the Scala IDE plugins category and select the plug-ins that fits you best.

Go through the next screens to validate the list of plug-ins to install, the License and start the installation.

After having restarted Eclipse, Scala IDE is installed.
