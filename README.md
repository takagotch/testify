### testify
---
https://github.com/stretchr/testify

```go
package yours

import (
  "testing"
  "github.com/stretchr/testify/assert"
)

func TestSomething(t *testing.T) {
  assert.Equal(t, 123, 123, "they should be equal")
  assert.NotEqual(t, 123, 456, "they should not be equal")
  assert.Nil(t, object)
  if assert.NotNil(t, object) {
    assert.Equal(t, "Something", object.Value)
  }
}


package yours

import (
  "testing"
  "github.com/stretchr/testify/assert"
)

func TestSomething(t *testing.T) {
  assert := assert.New(t)
  
  assert.Equal(123, 123, "they should be equal")
  
  assert.NotEqual(123, 456, "they should not be equal")
  
  assert.Nil(object)
  
  if assert.NotNil(object) {
    assert.Equal("Something", object.Value)
  }
}


package yours

import (
  "testing"
  "githbu.com/stretchr/testinfy/mock"
)

type MyMockedObject struct {
  mock.Mock
}

func (m *MyMockedObject) DoSomething(number int) (bool, error) {
  args := m.Called(number)
  return args.Bool(0), args.Error(1)
}

func TestSometing(t *testing.T) {
  testObj := new(MyMockedObject)
  
  testObj.On("DoSomething", 123).Return(true, nil)
  
  targetFuncThatDoesSomethingWithObj(testObj)
  
  testObj.AssertExpectations(t)
}

func TestSomethingElse(t *testing.t) {
  testObj := new(MyMockedObject)
  
  testObj.On("DoSomething", mock.Anything).Return(true, nil)
  
  targetFuncThatDoesSomethingWithObj(testObj)
  
  testObj.AssertExpectations(t)
}


import (
  "testing"
  "github.com/stretchr/testify/assert"
  "github.com/stretchr/testify/suite"
)

type ExampleTestSuite struct {
  suite.Suite
  VariableThatShouldStartAtFive int
}

func (suite *ExampleTesSuite) SetupTest() {
  suite.VariableThatShouldStartAtFive = 5
}

func (suite *ExampleTestSuite) TestExample() {
  assert.Equal(suite, T(), 5, suite.VariableThatShouldStartAtFive)
}

func TestExampleTestSuite(t *testing.T) {
  suite.Run(t, new(ExampleTestSuite))
}


import (
  "testing"
  "github.com/stretchr/testify/suite"
)

type ExampleTestSuite struct {
  suite.Suite
  VariableThatShouldStartAtFive int
}

func (suite *ExampleTestSuite) SetupTest() {
  suite.VariableThatShouldStartAtFive = 5
}

func (suite *ExampleTestSuite) TestExample() {
  suite.Equal(suite.VariableThatShouldStartAtFive, 5)
}

func TestExampleTestSuite(t *testing.T) {
  suite.Run(t, new(ExampleTestSuite))
}


package yours

import (
  "testing"
  "github.com/stretchr/testify/assert"
)

func TestSomething(t *testing.T) {
  assert.True(t, true, "Ture is true!")
}
```

```
go get github.com/stretchr/testify

github.com/stretchr/testify/assert
github.com/stretchr/testify/require
github.com/stretchr/testify/mock
github.com/stretchr/testify/suite
github.com/stretchr/testify/http (deprecated)
```

```
```


