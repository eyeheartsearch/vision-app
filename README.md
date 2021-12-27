Interact with the vision-app via Github Pages: 
https://eyeheartsearch.github.io/vision-app/

Powered by Algolia, the vision-app is the “public image search” section of a larger application where users can create their own vision boards. A vision board is a board (physical or digital) where people can add pictures and text that represent the things they intend to bring into their lives. For example, someone could add a picture of a traveler visiting a beach if they wish to travel more. The “public image search” section allows users to search for inspiration they can add to their own vision boards. 

The first thing I wanted was a rich and practical dataset composed of images that users can add to their vision boards. I wanted the dataset to include searchable attributes as well as custom ranking attributes I could experiment with. 

I wrote a script to create a dataset using the Pexels API:
https://www.pexels.com/api/documentation/#photos-search

Pexels is a stock photo and video library with millions of royalty-free and copyright-free images. The dataset was made from about 40 different categories, each containing 65-80 records totalling about 3000 records. The dataset included the following attributes:
image - a publicly available image url uniformly sized to 200h / 280w px.
category - (examples: adventure, family, wealth) - a searchable attribute  based on the search key of the Pexels API query. The refinement list/facets were also based on category. 
description - a searchable attribute, the title of the photo. 
photographer - a searchable attribute, the photographer of the photo. 
likes - A custom ranking attribute based on a number pseudo-randomly generated between 10 and 700.
saves - A custom ranking attribute based on a number pseudo-randomly generated between 10 and 150.

The experience was built using Algolia with React InstantSearch:
https://www.algolia.com/doc/guides/building-search-ui/what-is-instantsearch/react/

I was incredibly impressed by Algolia's performance and features. I used several of the widgets which made development enjoyable and easier to hit the ground running. The widgets utilized included SearchBox, Hits, Pagination, Highlight, ClearRefinements, RefinementList, and Configure. I enjoyed researching and configuring the widgets and I’m excited about how many features they include. It’s also nice how the widgets can be extended.

In the Algolia UI, the index configuration was intuitive and easy to use. I configured de-duplication based on the image URL which worked great when tested on the duplicate images. I experimented with things like typo tolerance and re-ordering searchable attributes. I experimented with the “like” and “save” custom ranking attributes which I generated with a pseudo-random number generator. I can see how custom attributes can be a powerful way to rank results if that data is available or if it can be calculated. 

One feature I could see being helpful in some cases is “calculated attributes” where formulas, other attributes, or a combination to calculate a new attribute is used for ranking. This could also help with data cleansing, for example if a user wants to remove "-" in attribute values and change them to " ". In either case, this can be accomplished programmatically and might be more of a wish list feature than a must have. 
