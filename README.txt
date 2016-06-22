Name:Kiran Bhat Gopalakrishna
Net Id:kxb140230

The code has been executed with spark-submit in local using sbt.


1)Place frinedlist file i.e soc-LiveJournal1Adj.txt in /user/hduser/input_friendlist
2)Place the userdata file i.e userdata.txt in /user/hduser/input_userdata
3)Place jar file in respective folders named q1/target,q2/target,q3/target,q4/target.
4)Run each of the following commands in the respective folders.


q1)spark-submit --class FriendRecommender  --master local target/scala-2.10/friend-recommender_2.10-1.0.jar /user/hduser/input_friendlist /user/hduser/output_q1

        Sample o/p : 8941    8944,8943,8940
                     9993    9991,13134,13877,34642,34485,13478,34299,37941
                     9990    13134,13877,34642,34485,13478,34299,37941
                     8942    8939,8944,8943,8940
                     9021    9023,9016,9020,317,9022,9017
                     9020    9023,9016,317,9021,9022,9017
                     9022    9023,9016,9020,9019,317,9021,9017
                     924     15416,439,43748,2409,45881,11860,6995
                     9992    9991,35667,9987,9989
                     9019    9023,317,902

q2)spark-submit --class MutualFriend  --master local target/scala-2.10/mutual-friends_2.10-1.0.jar /user/hduser/input_friendlist /user/hduser/output_hw1q2  14,15

q3) spark-submit --class MutualFriendDetails  --master local target/scala-2.10/mutual-friends-with-details_2.10-1.0.jar /user/hduser/input_friendlist /user/hduser/input_userdata /user/hduser/output_hw1q3  14,15

q4)$ spark-submit --class AverageAgeTop  --master local target/scala-2.10/average-age-top-20_2.10-1.0.jar /user/hduser/input_friendlist /user/hduser/input_userdata /user/hduser/output_q4
