.. The contents of this file may be included in multiple topics (using the includes directive).
.. The contents of this file should be modified in a way that preserves its ability to appear in multiple topics.


#. Open ``test/integration/default/serverspec/default_spec.rb``.
#. Add:

   .. code-block:: ruby
   
      require 'serverspec'
      set :backend, :exec
      
      describe 'apache' do
        it 'is awesome' do
          expect(true).to eq true
        end
        
        it 'is installed' do
          expect(package('httpd')).to be_installed
        end
      end

#. Save the file.
