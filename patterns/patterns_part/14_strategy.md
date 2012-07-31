!SLIDE small
    @@@ ruby
    class Post
      def send_to_feed
        if user.is_a?(TwitterUser)
          user.send_to_feed(contents)
        end
      end
    end
!SLIDE small
# Strategy pattern
!SLIDE small
    @@@ ruby
    class Post
      def send_to_feed
        user.send_to_feed(contents)
      end
    end

    class TwitterUser
      def send_to_feed(contents)
        twitter_client.post_to_feed(contents)
      end
    end

    class EmailUser
      def send_to_feed(contents)
        # no-op.
      end
    end
