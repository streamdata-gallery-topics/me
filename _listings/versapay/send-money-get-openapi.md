---
swagger: "2.0"
x-collection-name: VersaPay
x-complete: 0
info:
  title: VersaPay Single Payment Hosted Checkout
  description: |-
    Clients, customers, or donors, for instance, can send your organization money directly from their bank account or credit card simply by clicking a link which displays a page with your account name allowing your customer to make a payment to you for the specified dollar amount:
    <br>
    `https://secure.versapay.com/send_money?api_token={your_api_token}&amount={dollar_amount_for_customer_to_pay}`
    <br>
    Funds will go to the fund destination passed in the to_fund parameter. By default, the funds will be deposited into your default bank account once the transaction clears from the other party.
  contact:
    name: VersaPay Support
    url: https://www.versapay.com/support
    email: support@versapay.com
  version: 1.0.0
host: secure.versapay.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/debit_agreements:
    post:
      summary: Create an Agreement
      description: Create an agreement.
      operationId: createAgreement
      x-api-path-slug: apidebit-agreements-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Create
      - ""
      - Agreementss
  /api/debit_agreements/sent:
    get:
      summary: View Sent Agreements
      description: View sent agreements.
      operationId: viewSentAgreements
      x-api-path-slug: apidebit-agreementssent-get
      parameters:
      - in: query
        name: page
        description: 50 items are displayed per page
      responses:
        200:
          description: OK
      tags:
      - View
      - Sent
      - Agreements
  /api/debit_agreements/received:
    get:
      summary: View Received Agreements
      description: View received agreements.
      operationId: viewReceivedAgreements
      x-api-path-slug: apidebit-agreementsreceived-get
      parameters:
      - in: query
        name: page
        description: 50 items are displayed per page
      responses:
        200:
          description: OK
      tags:
      - View
      - Received
      - Agreements
  /api/debit_agreements/{token}/approve:
    post:
      summary: Approve an Agreement
      description: Approve an agreement.
      operationId: approveAgreement
      x-api-path-slug: apidebit-agreementstokenapprove-post
      parameters:
      - in: body
        name: fund_token
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: token
        description: The agreement identifier
      responses:
        200:
          description: OK
      tags:
      - Approve
      - Agreements
  /api/debit_agreements/{token}/cancel:
    post:
      summary: Cancel an Agreement
      description: Cancel an agreement.
      operationId: cancelAgreement
      x-api-path-slug: apidebit-agreementstokencancel-post
      parameters:
      - in: path
        name: token
        description: The agreement identifier
      responses:
        200:
          description: OK
      tags:
      - Cancel
      - Agreements
  /api/debit_agreements/{token}/reject:
    post:
      summary: Reject an Agreement
      description: Reject a *pending* agreement by supplying an agreement's *token*
        attribute and providing a *rejection_reason*.
      operationId: rejectAgreement
      x-api-path-slug: apidebit-agreementstokenreject-post
      parameters:
      - in: path
        name: token
        description: The agreement identifier
      responses:
        200:
          description: OK
      tags:
      - Reject
      - Agreements
  /api/debit_agreements/{token}/revoke:
    post:
      summary: Revoke an Agreement
      description: Revoke an *approved* agreement for your account by supplying an
        agreement's token attribute. The agreement's creator will no longer be able
        to debit your account using this agreement.
      operationId: revokeAgreement
      x-api-path-slug: apidebit-agreementstokenrevoke-post
      parameters:
      - in: path
        name: token
        description: The agreement identifier
      responses:
        200:
          description: OK
      tags:
      - Revoke
      - Agreements
  /send_money:
    get:
      summary: Single Payment Hosted Checkout
      description: |-
        Clients, customers, or donors, for instance, can send your organization money directly from their bank account or credit card simply by clicking a link which displays a page with your account name allowing your customer to make a payment to you for the specified dollar amount:
        <br>
        `https://secure.versapay.com/send_money?api_token={your_api_token}&amount={dollar_amount_for_customer_to_pay}`
        <br>
        Funds will go to the fund destination passed in the to_fund parameter. By default, the funds will be deposited into your default bank account once the transaction clears from the other party.
      operationId: hostedCheckout
      x-api-path-slug: send-money-get
      parameters:
      - in: query
        name: amount
        description: The amount in dollars that the transaction is for
      - in: query
        name: api_token
        description: A valid API token generated from your account
      - in: query
        name: link_url
        description: A url that gets stored and displayed on the transaction for an
          invoice
      - in: query
        name: locale
        description: Set the default language of the checkout, either `en` or `fr`
      - in: query
        name: message
        description: A message which will be stored with the transaction
      - in: query
        name: pref
        description: The preferred payment type either `ba` or `cc` for bank or credit
          card respectively
      - in: query
        name: reference
        description: Extra data (max 255 characters)
      - in: query
        name: return_to
        description: A url which will displayed to the user to return to your website
          after they finish the Signup and Confirmation
      - in: query
        name: to_fund
        description: The token of the bank account or balance where the funds should
          go to
      responses:
        200:
          description: OK
      tags:
      - Single
      - Payment
      - Hosted
      - Checkout
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---