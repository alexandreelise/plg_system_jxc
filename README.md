# JxC : Joomla! "multiplies" other CMS

## System - JxC : plg_system_jxc

> TLDR; JXC is system plugin to make Joomla! website synchronise with other CMS (Drupal, TYPO3, WordPress) via Web Services.

![visitor badge](https://visitor-badge.laobi.icu/badge?page_id=alexandreelise.plg_system_jxj&style=flat&format=true)
![GitHub followers](https://img.shields.io/github/followers/alexandreelise?style=flat)
![YouTube Channel Views](https://img.shields.io/youtube/channel/views/UCCya8rIL-PVHm8Mt4QPW-xw?style=flat&label=YouTube%20%40Api%20Adept%20vues)


<pre>

    __  __     ____         _____                              __                      __              
   / / / ___  / / ____     / ___/__  ______  ___  _____       / ____  ____  ____ ___  / ___  __________
  / /_/ / _ \/ / / __ \    \__ \/ / / / __ \/ _ \/ ___/  __  / / __ \/ __ \/ __ `__ \/ / _ \/ ___/ ___/
 / __  /  __/ / / /_/ /   ___/ / /_/ / /_/ /  __/ /     / /_/ / /_/ / /_/ / / / / / / /  __/ /  (__  ) 
/_/ /_/\___/_/_/\____/   /____/\__,_/ .___/\___/_/      \____/\____/\____/_/ /_/ /_/_/\___/_/  /____/  
                                   /_/                                                                 


</pre>

> ![GitHub Repo stars](https://img.shields.io/github/stars/alexandreelise/plg_system_jxj?style=flat) ![GitHub forks](https://img.shields.io/github/forks/alexandreelise/plg_system_jxj?style=flat) ![GitHub watchers](https://img.shields.io/github/watchers/alexandreelise/plg_system_jxj?style=flat)

Two latest release of 2 major version of each CMS supported (Drupal, Joomla, Typo3, WordPress) in alphabetical order
At the moment (2025-03-25), that means: Drupal (11.x,10x) , Joomla (5.x,4.x), TYPO3 (13.x, 12.x), WordPress (6.x, 5.x)

```

Joomla 4.x <-> Joomla 4.x
Joomla 4.x <-> Joomla 5.x
Joomla 4.x <-> Drupal 11.x
Joomla 4.x <-> Drupal 10.x
Joomla 4.x <-> TYPO3 13.x
Joomla 4.x <-> TYPO3 12.x
Joomla 4.x <-> WordPress 6.x
Joomla 4.x <-> WordPress 5.x

Joomla 5.x <-> Joomla 4.x
Joomla 5.x <-> Joomla 5.x
Joomla 5.x <-> Drupal 11.x
Joomla 5.x <-> Drupal 10.x
Joomla 5.x <-> TYPO3 13.x
Joomla 5.x <-> TYPO3 12.x
Joomla 5.x <-> WordPress 6.x
Joomla 5.x <-> WordPress 5.x

```

I called it JxC pronounced J "x" C because it's Joomla! multiplies other CMS, Joomla! website communicating with another
CMS of the [Open Website Alliance](https://openwebsitealliance.org/). That's it. Kinda like a CROSS JOIN for geeky database folks and girls.

## WHY?

My name is Alexandre J-S William ELISÉ, I am a French web developer and Joomla! specialist. The idea came from a demo I
needed to make for Virtual Joomladay France on Friday, June 12th 2020. A friend of mine, Marc DECHÈVRE, told me that it
would be great to make two Joomla! websites communicate together. I also wanted to contribute to the Joomla Web Services enhancement project but not as a student.
[GSoC 2025](https://docs.joomla.org/GSoC_2025_Project_Ideas)

## WHAT?

It is a unified system plugin that should work on both Joomla! 4.x and Joomla! 5.x

## HOW?

j3x -> j4x communication is using PHP streams to make an HTTP request to the j4x Web Service endpoint providing the api
token.
For j4x -> j3x communication it is more tricky because there are no webservices by default in Joomla! 3. That's why I
chose to use the com_api provided by Techjoomla for this purpose. If you would like to use another solution it is up to
you to change the code accordingly but I chose com_api for convenience, ease of use and efficiency. Feel free to use
what suits your use case the best.

### EDIT: Friday, July 14th 2023

> Now this plugin shift focus to make communication between j4x -> j5x and j4x <- j5x since j3x is close to EOL (End Of
> Life) which should be in August 2023

# INSTRUCTIONS

- Get the latest build in build directory or build it yourself by typing "make all" in your terminal after cloning this
  repository.
- Install the plugin on your website where the request comes from. For j3x --> j4x the request comes from j3x website so
  you install the plugin on your j3x website.
- Configure the plugin pay a special attention to base path and api token information. It's the information of the
  website where the request goes to. In the example above it's your j4x website. The category id is the category on the
  j4x website where you want to create articles. For now creating articles is the only action supported.
- On your j3x website go to your admin menu create an article and save it.
  onContentAfterSave the plugin will communicate with your j4x website using the secure token and create the same
  article there.
  -That's roughly how it works. Feel free to give your feedback and share your improvements.

## SPECIAL THANKS

I would like to say thanks to Marc DECHÈVRE for giving me the opportunity to share my knowledge of Joomla! publicly in a
live YouTube session on Friday, June 12th 2020. It's in French, but hopefully you will get the overall idea of what are
webservices in Joomla! 4.

## THANKS

- Techjoomla team for their cool extension com_api
- Joomla!
- Joomla! community for being so awesome

## CONTRIBUTORS

- Anyone is more than welcome to contribute to plg_system_jxc to make it even better.
  Take care. And have a delightful day. Super Joomlers!

--------------------------------------------

## INFOS

>
English: [Click here to get in touch](https://github.com/mralexandrelise/mralexandrelise/blob/master/community.md "Get in touch")

>
Français: [Cliquez ici pour me contacter](https://github.com/mralexandrelise/mralexandrelise/blob/master/community.md "Me contacter")
