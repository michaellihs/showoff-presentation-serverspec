!SLIDE title_slide

# Further Features #



!SLIDE code_slide

# Files

    @@@ ruby
    # be a file (not a directory)
    describe file('/etc/passwd') do
      it { should be_file }
    end

    # file exists
    describe file('/etc/passwd') do
      it { should exist }
    end

    # be a directory (not a file)
    describe file('/var/log/httpd') do
      it { should be_directory }
    end


!SLIDE code_slide

# Files (cont'd)

    @@@ ruby
    # file mode (permissions)
    describe file('/etc/sudoers') do
      it { should be_mode 440 }
    end

    # file owner
    describe file('/etc/sudoers') do
      it { should be_owned_by 'root' }
    end

    # md5 checksum (check for modifications)
    describe file('/etc/services') do
      its(:md5sum) { should eq '35435ea447...' }
    end


!SLIDE code_slide

# CRON Jobs

    @@@ ruby
    describe cron do
      it { should have_entry ↵
          '* * * * * /usr/local/bin/foo' }
    end


!SLIDE

# Resource Documentation

See http://serverspec.org/resource_types.html