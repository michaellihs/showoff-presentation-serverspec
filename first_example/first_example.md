!SLIDE title_slide

# First Example

## Is Apache Running? ##



!SLIDE code_slide

# Your First Test - a.k.a. Spec

    @@@ ruby

    
    describe service('httpd') do
      it { should be_enabled }
      it { should be_running }
    end

    describe port(80) do
      it { should be_listening }
    end



!SLIDE code_slide

# Run Your Test(s)

<pre class="sh_sourceCode"><code>
$ rake spec

Service "httpd"
  <span class="sh_fixed">should be enabled</span>
  <span class="sh_fixed">should be running</span>

Port "80"
  <span class="sh_fixed">should be listening</span>

Finished in 2.79 seconds ...
3 examples, 0 failures

</code></pre>
