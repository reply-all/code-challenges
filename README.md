Code Challenges
===============

A repository of common code challenges.

---

Build and deploy an app using angular on the client and node/express on the server.

The UI is a calculator and should look good and be responsive.

The client takes in the user input from the calculator and sends it off to server to do the logic, send the response back down, then render.

They were equally as interested in how you created a restful api, client-side validation and all the front end UI / UX stuff as they were w the logic done on the server to calculate the result of the input.

---

### Balanced Brackets

so given ```[ "(){}[]", "[{()}]", "{(}][)" ]```

How can return a boolean based on whether or not the parenthesis, square and curly brackets are balanced.

```ruby
require 'rspec'

def bool_brackets(str_of_br)
  addends = ["[", "{", "("]
  subends = ["]", "}", ")"]
  front_companion_from_end = {
    ")" => "(",
    "}" => "{",
    "]" => "["
  }
  stack = []

  str_of_br.split("").each do |x|
    if addends.include?(x)
      stack.push(x)
    elsif subends.include?(x)
      if stack[-1] == front_companion_from_end[x]
        stack.pop()
      else
        return false
      end
    else
      # ignore non-bracket chars
    end
  end

  stack.length == 0 ? true : false
end

describe "test brackets" do
  it "should return true for correct single bracket" do
    expect(bool_brackets("()")).to equal(true)
  end
  it "should return true for correct multiple brackets" do
    expect(bool_brackets("(){}[]")).to equal(true)
  end
  it "should return true for correct nested brackets" do
    expect(bool_brackets("({[]})[]")).to equal(true)
  end
  it "should return false for incomplete brackets" do
    expect(bool_brackets("()(")).to equal(false)
  end
  it "shoud return false for matching, but incorrectly ordered, front_companion_from_end" do
    expect(bool_brackets(")(")).to equal(false)
  end
end

```

---

It isn't as interesting or challenging but given a paragraph, rank the number of words used by frequency is a good starter

---

build an unbeatable tic tac toe game, build a form that validates credit card numbers, my friend did a challenge that he could only get to through making the right requests to an api

---

build a keyboard piano. interesting, not very challenging

---

one line fizz-buzz

```js
function fizzBuzz(l) {
    for(var i=1; i <= l; i++) {
        var s = i + ": ";
        if (i % 3 == 0) { s += "Fizz";}
        if (i % 5 == 0) { s += "Buzz";}
        console.log(s);
    }
}
fizzBuzz(100)
```

---

## Related Projects

* [github.com/uber/coding-challenge-tools](https://github.com/uber/coding-challenge-tools)
* [github.com/GasStationTV/angular-coding-exercise](https://github.com/GasStationTV/angular-coding-exercise)
