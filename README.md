# Restaurant GraphQL Exercise
## Title of project
Restaurant GraphQL Exercise
## Description of project
To set up GraphQL for the restaurant data and then add mutations to get and update these data. .
## How to run
npm install
go to localhost:5500/graphql and execute the mutations and queries:
mutation editrestaurants($idd: Int = 1, $name: String = "OLDO") {
  editrestaurant(id: $idd, name: $name) {
    name
    description
  }
}

mutation setrestaurants {
  setrestaurant(input: {
    name: "Granite",
    description: "American",
  }) {
    name
    description
  }
}

mutation deleterestaurants($iid: Int = 1) {
  deleterestaurant(id: $iid) {
    ok
  }
}

query getrestaurants {
  restaurants {
    name
    description
    dishes {
      name
      price
    }
  }
}
  
query getrestaurant($idd: Int = 1) {
	restaurant(id: $idd) {
 		name
  	description
  	dishes {
  	  name
   	 	price
  	}
	}
}

## Roadmap of future improvements
To incorporate Strapi for the database
## License information
MIT License

Copyright (c) 2023 lisayuan1001

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
