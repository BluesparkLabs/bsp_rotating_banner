# bsp_rotating_banner

bsp_rotating_banner is a D8 module that generates a simple Paragraph type,
a view and the Rotating Banner field. We can add the Rotating Banner field to a
content type and add the Node Rotating Banner block to a region. When we access
the node page we can see the Rotating Banner with the content from the
Paragraph.

___

We can install this module using Composer. Before using composer we need to add
the BluesparkLabs/bsp_rotating_banner and woothemes/flexslider repositories to
composer.json

        {
            "type": "vcs",
            "url": "https://github.com/BluesparkLabs/bsp_rotating_banner"
        },
        {
            "type": "package",
            "package": {
                "name": "woothemes/flexslider",
                "version": "2.6.3",
                "type": "drupal-library",
                "source": {
                    "url": "https://github.com/woothemes/FlexSlider.git",
                    "type": "git",
                    "reference": "2.6.3"
                }
            }
        }

Before installing we need to verify that we have "libraries" in our installer
 paths

        "installer-paths": {
            "web/libraries/{$name}": ["type:drupal-library"]
        }

 We only need to run "composer require bluesparklabs/bsp_rotating_banner" and
 all dependencies will be downloaded. Then from CLI we can run
 "drush en bsp_rotating_banner" to activate the module.

 We need to add the Rotating Banner field to a content type and then create
 content. We can add the rotating banner block from "/admin/structure/block".
 If we access a node page the rotating banner should appear.