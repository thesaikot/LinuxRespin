# LinuxRespin
Fork of remastersys - updates

This tool is used to backup your image, create distributions, create live cd/dvds.
install respin

If you are using Ubuntu - Consider switching to Debian.
This is NOT for Ubuntu.
Debian.
In the past, Ubuntu packages, dependency information and such was available. Thanks to a few choice words by some Ubuntu users, that changed on July 25, 2017!
Thank you.

Respin

- a script to create a livecd/dvd from a working Debian install

For more information, please visit http://www.linuxrespin.org


Limitations of remastering
========================== 

Due to some common questions I keep getting asked repeatedly I have put the answers here.

There are some limitations for remastering right now and they have absolutely nothing to do with Respin itself.

1 - Nvidia and ATI proprietary drivers are disabled at the kernel level by ubuntu's casper scripts - no workaround

2 - limit of 4Gig for any single file on the iso file which is a limitation of the iso9660 spec which means the 
compressed filesystem must be 4G or less - no workaround - Possible workaround with mkisofs

3 - no official text mode installer for the livecd so all remasters that you want to be able to install must have a gui
- no workaround

4 - Install options limited to what Ubuntu's installer, Ubiquity can do - no workaround

5 - In order for the Ubuntu casper scripts to create and boot into the livecd user, either gdm or kdm must be used
as the login manager - no workaround

6 - the livecd is limited to 1 iso file as casper only look for a single filesystem.squashfs file - no workaround

7 - compression level of the filesystem.squashfs doesn't have lzma as the Ubuntu kernel and mksquashfs would need
to be patched - unsupported/no workaround.

8 - livecd only works properly with linux-generic livecd kernel - if you make your own kernel you are on your own
- unsupported so please don't ask for help with this

9 - if it isn't in the normal Ubuntu repositories or requires a patch of an app that changes it from stock ubuntu apps
it is completely unsupported so please don't ask me for help with these

10 - there are certain apps and libraries that Ubuntu doesn't have on their livecd's and for whatever reason they
cause the livecd to fail if they are installed - no workaround

11 - if your customizations are not showing up on the livecd then it means you have not made the changes in the
correct place.  You must figure out what files need to be changed or where the global configuration of the settings
are that you are trying to change.  I only use KDE so I couldn't answer any gnome related questions anyway.
- you are on your own.

I have no intentions of maintaining a fork of casper or ubiquity or any other app so please don't ask me to change any of the above.  I make respin which helps you remaster a base Debian desktop live system and thats it.

These are not limitations of respin but rather the underlying tools that are used to remaster the
livecd/run the livecd/install the livecd.

These may change in the future if Ubuntu changes them but for now they are the limitations and there are no workarounds.

Respin simply builds the livecd from the system you are running.  If you have it setup correctly and
nothing conflicts with Ubuntu's casper or ubiquity then it should build, run and install just fine.

 
Information About Dist Mode for Ubuntu users (please see Launchpad for Ubuntu version)
=======================================================================================

The dist mode of respin is unsupported for the most part.

Respin works on Trisquel, Mint, LXLE, I have tested respin on stock installs of Ubuntu, Kubuntu and usually Xubuntu as well.

Normal i386 and amd64 versions so I know respin works on stock installs.

Most problems in dist mode are created by yourself due to customization or package choice.

These issues have nothing to do with remastersys.
They conflict with Ubuntu's casper livecd boot tool and Ubuntu's ubiquity installer and those aren't
going to be changed to suit your needs.  If you want to make changes to them, you will need to fork
those projects off on your own.




Regards,
Marcia 


---------------------------------------------------------------------------------------------------

u·bun·tu
ˌo͝oˈbo͝on(t)o͞o/
noun
Definition: I cannot configure Debian.

Sentence use: I do not care about community - I use Ubuntu! 

See also: Ughbuntu or Uhbuntu

There is a gui available. I will post this soon. 
Using the gui, you can change the boot screen. 

There is an Ubuntu developer on this project. His name is Chamuco.

So, if you need support or have suggestions, his project is on launchpad along with all accompanying files. 

Now, I'm focusing on Trisquel because a privacy lab at an Ivy league was asking about respin... and I'm all over that! Sorry Ubuntu users... you are on your own.

That being said, I think Ubuntu has some backup tools you could use.
Maybe something GUI based.

The problem here is I actually had some Ubuntu users demanding I make a server edition and make features for them.

Uh... yea. We are a community and not a company. If these users wanted to be a part of the community, this would be a different story.

... And the reason remastersys was abandoned and we picked up the project was because the dev was tired of being barraged by users like this requesting features.

It's open.
Make some!

The Ubuntu "community" has not even contributed one single line of code, not one single ";" to the Ubuntu version.

However, for the Debian version, someone wrote a front end, people did testing, they contributed ideas and code for opitmization.

The thing is ... Ubuntu is NOT a community distro. It's a business. You may as well use Winblows.

---------------------------------------------------------------------------------------------------

Remember, if you are creating a distro for public use, to use your own trademarked icons for the menu, etc. 
You can change these easily by researching the process for your particular base. 
You can change the plymouth theme also.

Maintaining a distro is important. 
Remember to build a community around your distro if that is what you want.

Customizing and creating distro can be fun and challenging. Also, this is a great way to learn more about distros and GNU Linux!


OPTIMIZING:
Is this relevant still... maybe
"Consider disabling Plymouth. If userspace boots in less than 1s, a boot splash is hardly useful, hence consider passing plymouth.enable=0 on the kernel command line. Plymouth is generally quite fast, but currently still forces settling device enumerations for graphics cards, which is slow. Disabling plymouth removes this bit of the boot." freedesktop.org
