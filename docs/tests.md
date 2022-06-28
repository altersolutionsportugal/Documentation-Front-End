# Tests

# Concept
 - Test Driven Development or TDD it's a technique used to develop software that relates to the concept of validation
 - The idea is that you should wirte the tests first and then implement the code to make them work
 - TDD it's executed in a cycle called red/green/refactor everything even a small increment must be tested.
 - You can read more about TDD here http://agiledata.org/essays/tdd.html

# Install Jest in your project

## Install

```shell
npm install --save-dev jest
```

# Define bussiness rules
- Must return the value of the products
- Must return the value of the product with discount
- Must return the value of the total of the products with discount

# Step 1
Create tests

```
describe('List', () => {
  it('Should return total value of products', () => {
    const products = [
      {price: 10},
      {price: 20},
    ]

    expect(list.sum(products)).toEqual(30)
  })

  it('Should return discount value of product', () => {
    const products = [
      {price: 10, discount: 1},
    ]

    expect(list.sum(products)).toEqual(9)
  })

  it('Should return total value of discount products', () => {
    const products = [
      {price: 10, discount: 1},
      {price: 20, discount: 1},
    ]

    expect(list.sum(products)).toEqual(28)
  })
})
```

# Rules
- At least 80%-90% of the application must be covered by tests
- Before a pull request that feature must be covered by tests
- Services don't need to be tested with the data from the BE
- Validation of templates by tests not required, but advised
