!SLIDE small
    @@@ ruby
    class Project
      def time_spent
        #long_method_to_calculate
      end

      def tasks
        #many objects
      end
    end
    time_spent = project.time_spent 
                   + tasks.time_spent
!SLIDE small
# Composition pattern

!SLIDE small
    @@@ ruby
    class Project
      has_many :tasks
      def time_spent
        tasks.sum(:time_spent)
      end
    end

    def CompositeTask < Task
      has_many :tasks
      def time_spent
        tasks.sum(:time_spent)
      end
    end

    class Task; def time_spent; 666 end end

    time_spent = project.time_spent
