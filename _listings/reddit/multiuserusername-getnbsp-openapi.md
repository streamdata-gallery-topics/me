---
swagger: "2.0"
x-collection-name: Reddit
x-complete: 0
info:
  title: Reddit Get Multi User Username
  description: Fetch a list of public multis belonging to username
  version: 1.0.0
host: www.reddit.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/me:
    get&nbsp;:
      summary: Get Me
      description: Returns the identity of the user currently authenticated via OAuth.
      operationId: get&nbsp;V1Me
      x-api-path-slug: v1me-getnbsp
      responses:
        200:
          description: OK
      tags:
      - Me
  /v1/me/karma:
    get&nbsp;:
      summary: Get Me Karma
      description: Return a breakdown of subreddit karma.
      operationId: get&nbsp;V1MeKarma
      x-api-path-slug: v1mekarma-getnbsp
      responses:
        200:
          description: OK
      tags:
      - Me
      - Karma
  /v1/me/prefs:
    get&nbsp;:
      summary: Get Me Prefs
      description: Return the preference settings of the logged in user
      operationId: get&nbsp;V1MePrefs
      x-api-path-slug: v1meprefs-getnbsp
      parameters:
      - in: query
        name: fields
        description: A comma-separated list of items from this set:default_theme_srthreaded_messageshide_downsemail_messagesprofile_opt_outshow_link_flaircreddit_autorenewshow_trendingprivate_feedsmonitor_mentionsresearchignore_suggested_sortemail_digestsmediaclickgadgetuse_global_defaultslabel_nsfwdomain_detailsshow_stylesheetslive_orangeredshighlight_controversialno_profanityemail_unsubscribe_alllanghide_upsallow_clicktrackinghide_from_robotscompressstore_visitsthreaded_modmaildesign_betabetaother_thememedia_previewover_18enable_default_themesgeopopularshow_promotemin_comment_scorepublic_votesno_video_autoplayorganiccollapse_read_messagesshow_flairmark_messages_readsearch_include_over_18hide_adsmin_link_scoretop_karma_subredditsnewwindownumsiteslegacy_searchnum_commentsshow_gold_expirationhighlight_new_commentsdefault_comment_sorthide_locationbar
        type: string
      responses:
        200:
          description: OK
      tags:
      - Me
      - Prefs
    patch&nbsp;:
      summary: Patch Me Prefs
      description: ""
      operationId: patch&nbsp;V1MePrefs
      x-api-path-slug: v1meprefs-patchnbsp
      parameters:
      - in: query
        name: This endpoint expects JSON data of this format
        description: '{  &quot;allow_clicktracking&quot;: boolean value,  &quot;beta&quot;:
          boolean value,  &quot;clickgadget&quot;: boolean value,  &quot;collapse_read_messages&quot;:
          boolean value,  &quot;compress&quot;: boolean value,  &quot;creddit_autorenew&quot;:
          boolean value,  &quot;default_comment_sort&quot;: one of (`confidence`,
          `top`, `new`, `controversial`, `old`, `random`, `qa`, `live`),  &quot;domain_details&quot;:
          boolean value,  &quot;email_digests&quot;: boolean value,  &quot;email_messages&quot;:
          boolean value,  &quot;email_unsubscribe_all&quot;: boolean value,  &quot;enable_default_themes&quot;:
          boolean value,  &quot;g&quot;: one of (`GLOBAL`, `US`, `AR`, `AU`, `BG`,
          `CA`, `CL`, `CO`, `HR`, `CZ`, `FI`, `GR`, `HU`, `IS`, `IN`, `IE`, `JP`,
          `MY`, `MX`, `NZ`, `PH`, `PL`, `PT`, `PR`, `RO`, `RS`, `SG`, `SE`, `TW`,
          `TH`, `TR`, `GB`, `US_WA`, `US_DE`, `US_DC`, `US_WI`, `US_WV`, `US_HI`,
          `US_FL`, `US_WY`, `US_NH`, `US_NJ`, `US_NM`, `US_TX`, `US_LA`, `US_NC`,
          `US_ND`, `US_NE`, `US_TN`, `US_NY`, `US_PA`, `US_CA`, `US_NV`, `US_VA`,
          `US_CO`, `US_AK`, `US_AL`, `US_AR`, `US_VT`, `US_IL`, `US_GA`, `US_IN`,
          `US_IA`, `US_OK`, `US_AZ`, `US_ID`, `US_CT`, `US_ME`, `US_MD`, `US_MA`,
          `US_OH`, `US_UT`, `US_MO`, `US_MN`, `US_MI`, `US_RI`, `US_KS`, `US_MT`,
          `US_MS`, `US_SC`, `US_KY`, `US_OR`, `US_SD`),  &quot;hide_ads&quot;: boolean
          value,  &quot;hide_downs&quot;: boolean value,  &quot;hide_from_robots&quot;:
          boolean value,  &quot;hide_locationbar&quot;: boolean value,  &quot;hide_ups&quot;:
          boolean value,  &quot;highlight_controversial&quot;: boolean value,  &quot;highlight_new_comments&quot;:
          boolean value,  &quot;ignore_suggested_sort&quot;: boolean value,  &quot;in_redesign_beta&quot;:
          boolean value,  &quot;label_nsfw&quot;: boolean value,  &quot;lang&quot;:
          a valid IETF language tag (underscore separated),  &quot;legacy_search&quot;:
          boolean value,  &quot;live_orangereds&quot;: boolean value,  &quot;mark_messages_read&quot;:
          boolean value,  &quot;media&quot;: one of (`on`, `off`, `subreddit`),  &quot;media_preview&quot;:
          one of (`on`, `off`, `subreddit`),  &quot;min_comment_score&quot;: an integer
          between -100 and 100,  &quot;min_link_score&quot;: an integer between -100
          and 100,  &quot;monitor_mentions&quot;: boolean value,  &quot;newwindow&quot;:
          boolean value,  &quot;no_profanity&quot;: boolean value,  &quot;no_video_autoplay&quot;:
          boolean value,  &quot;num_comments&quot;: an integer between 1 and 500,  &quot;numsites&quot;:
          an integer between 1 and 100,  &quot;organic&quot;: boolean value,  &quot;other_theme&quot;:
          subreddit name,  &quot;over_18&quot;: boolean value,  &quot;private_feeds&quot;:
          boolean value,  &quot;profile_opt_out&quot;: boolean value,  &quot;public_votes&quot;:
          boolean value,  &quot;research&quot;: boolean value,  &quot;search_include_over_18&quot;:
          boolean value,  &quot;show_flair&quot;: boolean value,  &quot;show_gold_expiration&quot;:
          boolean value,  &quot;show_link_flair&quot;: boolean value,  &quot;show_promote&quot;:
          boolean value,  &quot;show_stylesheets&quot;: boolean value,  &quot;show_trending&quot;:
          boolean value,  &quot;store_visits&quot;: boolean value,  &quot;theme_selector&quot;:
          subreddit name,  &quot;threaded_messages&quot;: boolean value,  &quot;threaded_modmail&quot;:
          boolean value,  &quot;top_karma_subreddits&quot;: boolean value,  &quot;use_global_defaults&quot;:
          boolean value,}'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Me
      - Prefs
  /v1/me/trophies:
    get&nbsp;:
      summary: Get Me Trophies
      description: Return a list of trophies for the current user.
      operationId: get&nbsp;V1MeTrophies
      x-api-path-slug: v1metrophies-getnbsp
      responses:
        200:
          description: OK
      tags:
      - Me
      - Trophies
  /v1/subreddit/emoji/emoji_name:
    delete&nbsp;:
      summary: Delete Subreddit Emoji Emoji Name
      description: |-
        Delete a Subreddit emoji.
        Remove the emoji from Cassandra and purge the assets from S3
        and the image resizing provider.
      operationId: delete&nbsp;V1SubredditEmojiEmojiName
      x-api-path-slug: v1subredditemojiemoji-name-deletenbsp
      responses:
        200:
          description: OK
      tags:
      - Subreddit
      - Emoji
      - Emoji
      - Name
  /v1/gold/gild/fullname:
    post&nbsp;:
      summary: Add Gold Gild Fullname
      description: fullname of a thing
      operationId: post&nbsp;V1GoldGildFullname
      x-api-path-slug: v1goldgildfullname-postnbsp
      parameters:
      - in: query
        name: fullname
        description: fullname of a thing
        type: string
      responses:
        200:
          description: OK
      tags:
      - Gold
      - Gild
      - Fullname
  /v1/gold/give/username:
    post&nbsp;:
      summary: Add Gold Give Username
      description: an integer between 1 and 36
      operationId: post&nbsp;V1GoldGiveUsername
      x-api-path-slug: v1goldgiveusername-postnbsp
      parameters:
      - in: query
        name: months
        description: an integer between 1 and 36
        type: string
      - in: query
        name: username
        description: A valid, existing reddit username
        type: string
      responses:
        200:
          description: OK
      tags:
      - Gold
      - Give
      - Username
  /by_id/names:
    get:
      summary: Get By Names
      description: Get a listing of links by fullname.
      operationId: get&nbsp;ByNames
      x-api-path-slug: by-idnames-get
      parameters:
      - in: query
        name: names
        description: A comma-separated list of link fullnames
        type: string
      responses:
        200:
          description: OK
      tags:
      - Names
  '{/r/subreddit}/comments/article':
    get&nbsp;:
      summary: Get Subreddit Comments Article
      description: Get the comment tree for a given Link article.
      operationId: get&nbsp;RSubredditCommentsArticle
      x-api-path-slug: rsubredditcommentsarticle-getnbsp
      parameters:
      - in: query
        name: article
        description: ID36 of a link
        type: string
      - in: query
        name: comment
        description: (optional) ID36 of a comment
        type: string
      - in: query
        name: context
        description: an integer between 0 and 8
        type: string
      - in: query
        name: depth
        description: (optional) an integer
        type: string
      - in: query
        name: limit
        description: (optional) an integer
        type: string
      - in: query
        name: showedits
        description: boolean value
        type: string
      - in: query
        name: showmore
        description: boolean value
        type: string
      - in: query
        name: sort
        description: one of (confidence, top, new, controversial, old, random, qa,
          live)
        type: string
      - in: query
        name: sr_detail
        description: (optional) expand subreddits
        type: string
      - in: query
        name: threaded
        description: boolean value
        type: string
      - in: query
        name: truncate
        description: an integer between 0 and 50
        type: string
      responses:
        200:
          description: OK
      tags:
      - Subreddit
      - Comments
      - Article
  /collapse_message:
    post&nbsp;:
      summary: Add Collapse Message
      description: Collapse a message
      operationId: post&nbsp;CollapseMessage
      x-api-path-slug: collapse-message-postnbsp
      parameters:
      - in: query
        name: id
        description: A comma-separated list of thing fullnames
        type: string
      - in: query
        name: uh / X-Modhash header
        description: a modhash
        type: string
      responses:
        200:
          description: OK
      tags:
      - Collapse
      - Message
  /read_all_messages:
    post&nbsp;:
      summary: Add Read All Messages
      description: Queue up marking all messages for a user as read.
      operationId: post&nbsp;ReadAllMessages
      x-api-path-slug: read-all-messages-postnbsp
      parameters:
      - in: query
        name: filter_types
        description: A comma-separated list of items
        type: string
      - in: query
        name: uh / X-Modhash header
        description: a modhash
        type: string
      responses:
        200:
          description: OK
      tags:
      - Read
      - Messages
  /read_message:
    post&nbsp;:
      summary: Add Read Message
      description: A comma-separated list of thing fullnames
      operationId: post&nbsp;ReadMessage
      x-api-path-slug: read-message-postnbsp
      parameters:
      - in: query
        name: id
        description: A comma-separated list of thing fullnames
        type: string
      - in: query
        name: uh / X-Modhash header
        description: a modhash
        type: string
      responses:
        200:
          description: OK
      tags:
      - Read
      - Message
  /uncollapse_message:
    post&nbsp;:
      summary: Add Uncollapse Message
      description: Uncollapse a message
      operationId: post&nbsp;UncollapseMessage
      x-api-path-slug: uncollapse-message-postnbsp
      parameters:
      - in: query
        name: id
        description: A comma-separated list of thing fullnames
        type: string
      - in: query
        name: uh / X-Modhash header
        description: a modhash
        type: string
      responses:
        200:
          description: OK
      tags:
      - Uncollapse
      - Message
  /unread_message:
    post&nbsp;:
      summary: Add Unread Message
      description: A comma-separated list of thing fullnames
      operationId: post&nbsp;UnreadMessage
      x-api-path-slug: unread-message-postnbsp
      parameters:
      - in: query
        name: id
        description: A comma-separated list of thing fullnames
        type: string
      - in: query
        name: uh / X-Modhash header
        description: a modhash
        type: string
      responses:
        200:
          description: OK
      tags:
      - Unread
      - Message
  /message/where:
    get&nbsp;:
      summary: Get Message Where
      description: This endpoint is a listing.
      operationId: get&nbsp;MessageWhere
      x-api-path-slug: messagewhere-getnbsp
      parameters:
      - in: query
        name: after
        description: fullname of a thing
        type: string
      - in: query
        name: before
        description: fullname of a thing
        type: string
      - in: query
        name: count
        description: 'a positive integer (default: 0)'
        type: string
      - in: query
        name: limit
        description: 'the maximum number of items desired (default: 25, maximum: 100)'
        type: string
      - in: query
        name: mark
        description: one of (true, false)
        type: string
      - in: query
        name: mid
        type: string
      - in: query
        name: show
        description: (optional) the string all
        type: string
      - in: query
        name: sr_detail
        description: (optional) expand subreddits
        type: string
      responses:
        200:
          description: OK
      tags:
      - Message
      - Where
  /mute_message_author:
    post&nbsp;:
      summary: Add Mute Message Author
      description: For muting user via modmail.
      operationId: post&nbsp;MuteMessageAuthor
      x-api-path-slug: mute-message-author-postnbsp
      parameters:
      - in: query
        name: id
        description: fullname of a thing
        type: string
      - in: query
        name: uh / X-Modhash header
        description: a modhash
        type: string
      responses:
        200:
          description: OK
      tags:
      - Mute
      - Message
      - Author
  /unmute_message_author:
    post&nbsp;:
      summary: Add Unmute Message Author
      description: For unmuting user via modmail.
      operationId: post&nbsp;UnmuteMessageAuthor
      x-api-path-slug: unmute-message-author-postnbsp
      parameters:
      - in: query
        name: id
        description: fullname of a thing
        type: string
      - in: query
        name: uh / X-Modhash header
        description: a modhash
        type: string
      responses:
        200:
          description: OK
      tags:
      - Unmute
      - Message
      - Author
  /multi/rename:
    post&nbsp;:
      summary: Add Multi Rename
      description: Rename a multi.
      operationId: post&nbsp;MultiRename
      x-api-path-slug: multirename-postnbsp
      parameters:
      - in: query
        name: display_name
        description: a string no longer than 50 characters
        type: string
      - in: query
        name: from
        description: multireddit url path
        type: string
      - in: query
        name: to
        description: destination multireddit url path
        type: string
      - in: query
        name: uh / X-Modhash header
        description: a modhash
        type: string
      responses:
        200:
          description: OK
      tags:
      - Multi
      - Rename
  /multi/user/username:
    get&nbsp;:
      summary: Get Multi User Username
      description: Fetch a list of public multis belonging to username
      operationId: get&nbsp;MultiUserUsername
      x-api-path-slug: multiuserusername-getnbsp
      parameters:
      - in: query
        name: expand_srs
        description: boolean value
        type: string
      - in: query
        name: username
        description: A valid, existing reddit username
        type: string
      responses:
        200:
          description: OK
      tags:
      - Multi
      - User
      - Username
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