+++
title = "Processing with IoT Core"
date = 2021-05-03T13:44:16-05:00
weight = 100
chapter = false
+++

### In this module you will learn how AWS IoT Core can receive position updates for a customer device and process them with Amazon Location.

1. Open the Lambda console and edit the function called "lbs_simulate_customers". Comment out the line near line 96 that called "publish_location".

    `# publish_location(device)`

    and uncomment the line near line 99 that calls "publish_location_iot"

    `publish_location_iot(device)`

1. Deploy the function code changes to save them.  

1. Using a second browser window, navigate to the AWS IoT console and open the **Test** page. Subscribe to all topics using the wildcard **#** character.

    ![iot_core_test](/iot_core_test.png?width=50pc)

1. Run the 'lbs_simulate_customers' Lambda function using the default test event and immediately switch to the IoT Core test page to check if MQTT messages are arriving.

    ![iot_core_test_results](/iot_core_test_results.png?width=50pc)

1. Add an IoT Core Rule that forwards customer device position updates to the 'lbs_update_tracker' Lambda function. Click on **Rules** on the left and then enter the name **lbs_customer_device_update** with a topic filter of
`customers/#`

    ![iot_core_rule](/iot_core_rule.png?width=50pc)

    ![iot_core_rule2](/iot_core_rule2.png?width=50pc)

1. Add a Rule Action for a Lambda function and select the 'lbs_update_tracker' function from the list.

    ![iot_core_rule_action](/iot_core_rule_action.png?width=50pc)

    ![iot_core_rule_action2](/iot_core_rule_action2.png?width=50pc)

    ![iot_core_rule_action3](/iot_core_rule_action3.png?width=50pc)

1. Save the new rule by clicking **Create Rule**.

    ![iot_core_rule_action4](/iot_core_rule_action4.png?width=50pc)

1. Re-test the simulation by running the default test event and observing updates in DynamoDB as before. Updates should be occurring just as they had before, but now via MQTT with IoT Core.
