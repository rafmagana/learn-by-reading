!SLIDE section

Ways to understand code

!SLIDE bullets incremental

* Implement a feature  
* Fix a bug
* Write tests  

!SLIDE big reason

Tests

!SLIDE

	@@@ ruby
	%w[Ruby C ObjC JS Bash PHP .NET].take(5)

!SLIDE smaller

https://github.com/ruby/ruby/blob/trunk/test/ruby/test_array.rb

	@@@ ruby
	require 'test/unit'
	
	class TestArray < Test::Unit::TestCase
		...
		def test_take
			assert_equal([1,2,3], [1,2,3,4,5,0].take(3))
			...
		end
		...
	end

!SLIDE smaller

https://github.com/rubyspec/rubyspec/blob/master/core/array/take_spec.rb

	@@@ ruby
	describe "Array#take" do

	    it "returns the first specified number of elements" do
	
	      [1, 2, 3].take(2).should == [1, 2]
	
	    end

		...

	end

!SLIDE big reason

no test suite?

!SLIDE big reason

*Write it*

!SLIDE big reason

Paired reading

.notes Talk about Pair programming and Code reviewing

!SLIDE big reason

Read OSS

!SLIDE

	@@@ ruby
	%w[Ruby C ObjC JS Bash PHP .NET].take(5)

!SLIDE smaller

https://github.com/ruby/ruby/blob/trunk/array.c:4914
	
	@@@ ruby
	void
	Init_Array(void)
	{
		...
		
		rb_cArray  = rb_define_class("Array", rb_cObject);
		
		rb_include_module(rb_cArray, rb_mEnumerable);
		
		...
		
		rb_define_method(rb_cArray, "take", rb_ary_take, 1);
	}

!SLIDE smaller

https://github.com/ruby/ruby/blob/trunk/array.c:4598

	@@@ ruby
	rb_ary_take(VALUE obj, VALUE n)
	{
	    long len = NUM2LONG(n);
	    if (len < 0) {
		rb_raise(rb_eArgError, "attempt to take negative size");
	    }
	    return rb_ary_subseq(obj, 0, len);
	}