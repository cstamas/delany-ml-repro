See https://lists.apache.org/thread/cr5sh5tbz5fd2kqqf65stgtlbkj3zl98

# Steps

$ mvn -Dmaven.repo.local=local compile

This fails, as no snapshot. Nuke local repo.

$ mvn -Dmaven.repo.local=local compile -P profile-a

This will work.

$ mvn -Dmaven.repo.loca=local compile -P profile-b

This will also work, but Resolver will recheck the availability.


