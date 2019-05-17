Lab 1: Solution
===============

##### entitySearch

    {
      actor {
        entitySearch(query: "name = 'New Relic Pet Clinic' and domain = 'BROWSER'") {
          results {
            entities {
              accountId
              guid
              name
              domain
            }
          }
        }
      }
    }

##### taggingAddTagsToEntity

    mutation {
      taggingAddTagsToEntity(
        guid: "MXxC...U3Nw", 
        tags: {key: "training", values: [ "Your Name" ]}) {
        errors {
          message
          type
        }
      }
    }

##### entity (view tags)

    {
      actor {
        entity(guid: "MXxC...U3Nw") {
          tags {
            key
            values
          }
        }
      }
    }