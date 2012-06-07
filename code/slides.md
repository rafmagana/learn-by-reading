!SLIDE section

Let's talk about code

.notes Why would we expect to write good code if we have never read any great code?

!SLIDE medium reason

Programming not only  
has to do with writing code,  
but with reading it too.

!SLIDE medium reason

A lot of good things may  
result from you writing code

!SLIDE medium reason

Make you a better  
programmer is not one of them

!SLIDE medium reason

If you write 1000 LoC a day  
<b>you will not improve</b>

!SLIDE big reason

How do you learn?

.notes ask people to answer the question

!SLIDE big reason

Read somebody else's code

!SLIDE big reason

Somebody better than you!

!SLIDE big reason

Read your own old code

!SLIDE big reason

Read ugly code

!SLIDE big reason

Read good code

!SLIDE big reason

You will end up  
telling the difference

!SLIDE big reason

Code is way easier to   
write than it is to read

!SLIDE medium reason

Let's start with the hard part!

!SLIDE smaller

	@@@ ruby
	learn_it = ->(lang) do
		puts "want to learn #{lang}? Read code written in #{lang}"
	end

!SLIDE smaller

	@@@ ruby
	learn_it = ->(lang) do
		puts "want to learn #{lang}? Read code written in #{lang}"
	end

	%w[Ruby C ObjC JS Bash PHP .NET].take(5).each &learn_it

!SLIDE smaller

	@@@ ruby
	learn_it = ->(lang) do
		puts "want to learn #{lang}? Read code written in #{lang}"
	end

	%w[Ruby C ObjC JS Bash PHP .NET].take(5).each &learn_it

<pre>
want to learn Ruby? Read code written in Ruby  
want to learn C? Read code written in C  
want to learn ObjC? Read code written in ObjC  
want to learn JS? Read code written in JS  
want to learn Bash? Read code written in Bash
</pre>