# BYOB, part 2

We need to change the way the file stores the information, because it turns out to not really be manageable. You'll see: you will have to re-enter the stuff you've put in there since last week... But now, we're going to use CSV, which is a much more robust and computer-friendly format, which will allow us to modify this code much more easily in the future.

Ruby, thankfully, comes with a built-in CSV parser and writer, so you can just `require 'csv'`, read the docs and get to work.

The tests in `1_1_textbook_test.rb` are obsolete, so that file can just be deleted. They are replaced by the tests in `2_1_texbook_test.rb`. You will need to modify the `textbook.rb` file. The tests will guide you.

We introduce the idea of "fixtures" here. They are test data, useful for tests, to keep the tests simple. The fixtures are also simple, so that you as a developer don't have to deal with too much mental overhead.

Now, this makes running the tests a little stricter: they **MUST** be run from **the root of the project directory** (that is, from the directory that has lib/ and test/ ). This is a matter of relative paths. Making the tests more flexible means more complex code.

Because I kept the tests simpler, you could be clever and not use CSV. Don't be clever. Use CSV. Using CSV is not clever. It is smart. Clever is bad.

There are bonus tests here. You do not HAVE to make them pass, but if you do, you can pat yourself on the back! They are commented out right now.
In order to make them pass, you will need to do a `require_relative 'page'` in the `textbook.rb` file.

The Sinatra tests are not optional. Create a `config.ru` file the way you have in class (this is something you can Google).
You will want to look at how to create settings in Sinatra, over here: http://www.sinatrarb.com/configuration.html

You can refer to the Sinatra lesson from Thursday afternoon.

Keep in mind Matt's lesson on Post-Redirect-Get.

Don't be afraid to Google when it comes to things related to `last_response`.
