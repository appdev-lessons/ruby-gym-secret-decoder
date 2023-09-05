# Ruby Gym: Secret Decoder

We have a program to encode our messages, now can you write a way to decode them? 

Remember our secret code, don't tell anyone: 

    a = 1, e = 2, i = 3, o = 4, u = 5


Your program should:
- take an encoded message
- decode the message
- print the decoded message.

Make sure each of these the `secret` strings below output the correct encoded response, then get the tests to pass.

```ruby
secret = [
  "3 h1v2 1 s2cr2t t4 sh1r2",
  "3s th3s s2c5r2 2n45gh f4r my P1SSW4RD?",
  "w2 sh45ld b2 m4r2 cl2v2r"
].sample
pp secret
# write your program below
```
{: .repl #secret_decoder title="Secret Decoder" readonly_lines="[1,2,3,4,5,6,7]"}


```ruby
describe "Secret Decoder" do
  it "prints 'You and i need to be more secret', when the input is 'Y45 1nd 3 n22d t4 b2 m4r2 s2cr2t'" do
    path = "/tmp/code.rb"
    allow_any_instance_of(Array).to receive(:sample).and_return("Y45 1nd 3 n22d t4 b2 m4r2 s2cr2t")
    expect { require_relative(path) }.to output(/You and i need to be more secret/i).to_stdout
  end
end
```
{: .repl-test #secret_decoder_test_1 for="secret_decoder" title="Secret Decoder prints 'You and i need to be more secret', when the input is 'Y45 1nd 3 n22d t4 b2 m4r2 s2cr2t'" points="1"}

```ruby
describe "Secret Decoder" do
  it "prints 'Don't tell anyone our code', when the input is 'D4n't t2ll 1ny4n2 45r c4d2'" do
    path = "/tmp/code.rb"
    allow_any_instance_of(Array).to receive(:sample).and_return("D4n't t2ll 1ny4n2 45r c4d2")
    expect { require_relative(path) }.to output(/Don't tell anyone our code/i).to_stdout
  end
end
```
{: .repl-test #secret_decoder_test_2 for="secret_decoder" title="Secret Decoder prints 'Don't tell anyone our code', when the input is 'D4n't t2ll 1ny4n2 45r c4d2'" points="1"}
