Understanding the current website
-----
The current website seems to contain a basic landing page with information about the program. Enable to access the educational information you have to login with your ID (no password). Once logged in, there are 23 educational sections:
- Adult Portion Sizes (adult_portion_sizes)
- Breastfeeding Promotion (breastfeeding_promotion)
- Cooking Fast Healthy Meals ()
- Dental Care for Pregnant Women and Infants ()
- Dental Care for Toddlers and Preschoolers ()
- Family Mealtime ()
- Feeding Your Older Infant ()
- Feeding Your Preschooler ()
- Feeding Your Toddler ()
- Feeding Your Younger Infant ()
- How to Breastfeed ()
- Junk Food, Snacks and Eating Out ()
- Healthy Weight in Children ()
- Physical Activity ()
- Picky Eaters ()
- Portion Sizes for Preschoolers ()
- Portion Sizes for Toddlers ()
- Postpartum Nutrition and Weight Loss ()
- Pregnancy and Nutrition ()
- Smart Shopping (smart_shopping)
- Supporting Continued Breastfeeding ()
- Vegetables and Gardening ()
- Weaning

Each one of these sections uses basic Flash swf files and passes in XML files to load information for each one.

Basic XML structure
-----
Each section has a title, a "question," and a description towards the top. On the bottom left, you'll see a list of the main content needed for Nutrition Education for Credit (NEC). To the right of that are optional units with additional material not required to get credit. 

INSERT IMAGE HERE

The `<interface_text>` section provides basic descriptors for the areas, but not sure where it shows up on the page just yet.

The `<preload_que>` section has a list of all the resources (presumably to download to the browser). These include images, SWF (Flash) files, and more XML files.

The `<nec_pathway>` section provides details about the steps that need to be completed to get credit (`<required_items nec_path_length="25">` where 25 is the estimated time in minutes to complete the tasks) in addition to the optional components (`<optional_items>`). In the NEC required component, there are different tasks available:
- Pre-test
- Feature
- Challenge
- Discover
- Activities
- Test

For each of these, it'll load XML and SWF files as needed. $MODULE_NAME is the educational section (e.g. 'smart_shopping'). $MODULE_LANGUAGE is either 'english' or 'spanish.'

Pre-test
-----
tests/$MODULE_NAME/$MODULE_LANGUAGE/pretest.xml
[Explanation](pre-test.md)

Feature
-----
expert/$MODULE_NAME/$MODULE_LANGUAGE/expert.xml
[Explanation](expert.md)

Challenge
-----
challenge/$MODULE_NAME/$MODULE_LANGUAGE/challenge.xml
[Explanation](challenge.md)

Discover
-----
discover/$MODULE_NAME/$MODULE_LANGUAGE/discover.xml
[Explanation](discover.md)

Activities
-----
activities/$MODULE_NAME/xml/$MODULE_LANGUAGE/activities.xml
[Explanation](activities.md)

Test
-----
tests/$MODULE_NAME/$MODULE_LANGUAGE/test.xml
[Explanation](test.md)