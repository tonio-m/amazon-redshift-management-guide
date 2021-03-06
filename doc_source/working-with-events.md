# Amazon Redshift events<a name="working-with-events"></a>

**Topics**
+ [Overview](#working-with-events-overview)
+ [Viewing events using the console](viewing-events-console.md)
+ [Viewing events using the AWS SDK for Java](managing-events-java.md)
+ [Viewing events using the Amazon Redshift CLI and API](view-events-api-cli.md)
+ [Amazon Redshift event notifications](working-with-event-notifications.md)

## Overview<a name="working-with-events-overview"></a>

Amazon Redshift tracks events and retains information about them for a period of several weeks in your AWS account\. For each event, Amazon Redshift reports information such as the date the event occurred, a description, the event source \(for example, a cluster, a parameter group, or a snapshot\), and the source ID\. 

Amazon Redshift provides notification in advance for some events\. These events have an event category of `pending`\. For example, we send an advance notification if a hardware update is required for one of the nodes in your cluster\. You can subscribe to pending events the same as other Amazon Redshift events\. For more information, see [Subscribing to Amazon Redshift event notifications](working-with-event-notifications.md#working-with-event-notifications-subscribe)\. 

You can use the Amazon Redshift Management Console, the Amazon Redshift API, or the AWS SDKs to obtain event information\. You can obtain a list of all events, or you can apply filters, such as event duration or start and end date, to obtain events information for a specific period\. You can also obtain events that were generated by a specific source type, such as cluster events or parameter group events\.

You can create Amazon Redshift event notification subscriptions that specify a set of event filters\. When an event occurs that matches the filter criteria, Amazon Redshift uses Amazon Simple Notification Service to actively inform you that the event has occurred\.

For a list of Amazon Redshift events by source type and category, see [Amazon Redshift event categories and event messages](working-with-event-notifications.md#redshift-event-messages)