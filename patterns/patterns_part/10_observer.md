!SLIDE small
    @@@ ruby
    class User < ActiveRecord::Base

      def save
        super.save
        send_welcome_email
      end
    end

!SLIDE small
# Observer pattern
!SLIDE small
    @@@ ruby
    class User < ActiveRecord::Base
      def save
        super.save
      end
    end

    class UsrObserver < ActiveRecord::Observer
      observe :user
      def after_save(user)
        user.send_welcome_email
      end
    end
    #OR
    class User < ActiveRecord::Base
      after_save :send_welcome_email
    end
