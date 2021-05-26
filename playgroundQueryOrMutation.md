# Write your query or mutation here
```graphql
mutation createCategory{
  createCategory(input:{ name: "frontend",description:"front end category"}){
    id,
    name,
    description
  }
}

mutation createCourse{
  createCourse(
    input:{
    name: "React",
    description: "crouse about lib ReactJs",
    categoryId: "T%d5577006791947779410"
    }){
    id,
    name,
    category{
      id,
      name
    }
  }
}

mutation createChapter {
  createChapter(input: {
    name: "lesson 1",
    courseId: "T%d8674665223082153551"
  }){
    id,
    name,
    course{
      name
    }
  }
}

query findCategories {
  categories{
    id,
    name,
    description
  }
}

query findCourses {
  courses{
    id,
    name
  },
  categories {
    name,
    courses {
      name
    }
  }
}

query findChapters {
  chapters{
    id,
    name,
    course {
      name
    }
  }
}

```