!SLIDE small
    @@@ ruby
    class User
      attr_accessor :first_name, :last_name

      def display_name
        "#@first_name #@last_name"
      end
    end
!SLIDE small
# Decorator pattern

!SLIDE small
    @@@ ruby
    class UserDecorator
      def initialize(user)
        @user = user
      end

      delegate :first_name, 
        :last_name to: @user

      def display_name
        "#@first_name #@last_name"
      end
    end

