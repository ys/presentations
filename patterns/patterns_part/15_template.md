!SLIDE small
    @@@ ruby
    class Tartiflette
      def do_the_meal
        #long_gaz_opening
        #lighter.burn
        #frozen_box.open_the_box
        #put_on_dishes
      end
    end
!SLIDE small
#Template pattern
!SLIDE small
    @@@ ruby
    class Recipe
      def do_the_meal
        turn_on_fire; cook; serve
      end
    end

    class Tartiflette < Recipe
      def turn_on_fire
        #long_gaz_opening
      end
      def cook
        #frozen_box.open_the_box
      end
      def serve
        #put_on_dishes
      end
    end
!SLIDE
<img src='http://blog.yannick.io/images/ruby.png'/>
