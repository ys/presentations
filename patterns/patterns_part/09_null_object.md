!SLIDE small
    @@@ ruby
    def street_name(user)
      if user.address
        user.address.street_name
      else
        'No street name on file'
      end
    end
!SLIDE small
# Null Object pattern
!SLIDE small
    @@@ ruby
    def street_name(user)
      user.address.street_name
    end

    class User
      def address
        @address || NullAddress.new
      end
    end

    class NullAddress
      def street_name
        'No street name on file'
      end
    end
!SLIDE
<img src='http://blog.yannick.io/images/ruby.png'/>
