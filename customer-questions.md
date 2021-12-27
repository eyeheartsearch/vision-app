Question 1: Hello,

I'm new to search engines, and there are a lot of concepts I'm not educated on. To make my onboarding smoother, it'd help if you could provide me with some definitions of the following concepts:

Records
Indexing
I'm also struggling with understanding what types of metrics would be useful to include in the "Custom Ranking."

**Answer 1:**

Hi George, 
These are excellent questions. We’re excited to begin working with you and the team. Hopefully these answers can help clarify some core Algolia concepts as you begin onboarding. 

**Record**: A record is a single entry that appears in the search. Since your company runs an e-commerce movie store, a record would be a single movie and the record should contain key-value pairs of attributes that includes any information that facilitates search, displays on the front end, filtering, or relevance. You can leave everything else out. 
Looking at your app, here is an example of what a single record might include. This is just an example and you want to include/exclude the attributes that best meet your needs and meet the key-value pair criteria described above.

{
  "title": "movie-title-here",
  “Description”: “movie-description”,
  "year": "movie-image",
  “actors-and-actresses”: [“actor-1”, “actor-2”]
  "image": "movie-image-public-url”,
  "downloads": # of downloads,
  "sales": # of sales,
  “rentals: # of rentals,
  "categories": ["horror", "thriller", "suspense"],
  "adults only": false
}

Read more about records here:
https://www.algolia.com/doc/guides/sending-and-managing-data/prepare-your-data/#algolia-records

**Indexing**:  An index is where your records in Algolia are stored. So if a record contains the attributes for a movie, an index contains the total set of records (all movies) that can appear in a search. Records are sent to and then indexed in Algolia and Algolia indexes optimize the records for search operations. 
Records need to be structured before they are indexed in Algolia. You can prepare your data for indexing following these articles:
https://www.algolia.com/doc/guides/sending-and-managing-data/prepare-your-data/
https://www.algolia.com/doc/guides/sending-and-managing-data/prepare-your-data/in-depth/prepare-data-in-depth/

**Metrics to include in custom ranking**: If you want to have the most popular movies to appear first in your search results, then you can consider using some attributes for custom ranking. These attributes need to be numeric or boolean (true/false). For example, if you use “rentals” as a custom ranking attribute, movies that are rented more would be displayed in search before movies that are rented less.
You may also use multiple custom ranking attributes. Read more about custom ranking here: 
https://www.algolia.com/doc/guides/sending-and-managing-data/prepare-your-data/#attributes-for-customizing-ranking

Please let me know if you have additional questions!

Thanks,
Mike

Cheers, George

Question 2: Hello,

Sorry to give you the kind of feedback that I know you do not want to hear, but I really hate the new dashboard design. Clearing and deleting indexes are now several clicks away. I am needing to use these features while iterating, so this is inconvenient.

Regards, Matt

**Answer 2:**

Hi Matt, 

It does take a few clicks to delete and clear indexes in the dashboard. I believe this was partly a safety feature to prevent indexes from being deleted inadvertently in the dashboard.

You can delete/clear indexes more quickly while iterating by using the API. Please refer to the docs below:
**Delete Index by API**: https://www.algolia.com/doc/api-reference/api-methods/delete-index/
**Clear Index by API**: https://www.algolia.com/doc/api-reference/api-methods/clear-objects/

Let me know if this information helps or if you would like us to submit a product feedback ticket. Please never hesitate to share feedback, it’s always appreciated. It’s important for us to let our product team know any challenges you are facing in your workflow. For future reference, you can add feedback directly to our community discourse. https://discourse.algolia.com/c/feedback/3

Thanks,
Mike


Question 3: Hi,

I'm looking to integrate Algolia in my website. Will this be a lot of development work for me? What's the high level process look like?

Regards, Leo

**Answer 3:**

Hi Leo, 

That’s great to hear! I’m happy to serve as a resource for answering any of your questions as you get up and running. We generally find that integrating doesn’t take too much development work and we’re here to help you get started so you can start leveraging Algolia’s rich set of features. 

The high level process for integration looks like this: 
1. Send your search data to an Algolia index and configure the index.
https://www.algolia.com/doc/guides/sending-and-managing-data/send-and-update-your-data/
2. Integrate Algolia into your search UI
https://community.algolia.com/#instantsearch 

Let's set up a call to discuss your website and talk through the integration steps and your goals with Algolia in more detail. Please let me know some times this week that work for you or feel free to add an hour to my Calendly. 

Thanks,
Mike
