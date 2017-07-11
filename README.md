We can install this module using composer. Before using composer we need to add
 the BluesparkLabs and woothemes/flexslider repositories.

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

Before installing we need to verify that we have libraries in our installer paths

        "installer-paths": {
            "web/libraries/{$name}": ["type:drupal-library"]
        }

 We only need to run "composer require bluesparklabs/bsp_rotating_banner" and
 all the dependencies will be installed. Then from CLI we can run
 "drush en bsp_rotating_banner".

 We need to add the Rotating Banner field to a content type and then add content.
 We can add the rotating banner block from "/admin/structure/block". If we
 access a node page the rotating banner will appear.