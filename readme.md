# ADJEMIN SMS CAMPAIGN

This repository provides suitables tools for performing sms campaign. Actually, only Api's from MTN SMS CLOUD are embedded.

## Architecture

This repo has two main classes

  - **BaseApi** in `./core/BaseApi.php`
  - **MTNSMSApi** in `./MTNSMSApi.php`

## Development

Be sure to check the namespace first.

### Instanciation

```php
require_once "./MTNSMSApi.php";

/**
 * Create a new Instance
 * 
 * @param string $sender_id = The desired sender_id
 * @param string $token = $token associated with $sender_id 
 */
$msa = new MTNSMSApi($sender_id, $token);

/**
 * Send a new Campaign
 * 
 * @param array $recipients {Ex: ["225xxxxxxxx", "225xxxxxxxx"]}
 * @param string $message
 */
return $msa->newCampaign($recipients, $message);

/**
 * Retrieves on created Campaign
 * 
 * @param string $campaign_id
 * @param string $message
 */
return $msa->getCampaign($campaign_id, $message);

```
