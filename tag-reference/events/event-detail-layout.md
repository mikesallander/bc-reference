## Event Detail Layout

### Location
* **Admin Console:** Site Manager > Module Templates > Event Layouts > Detail Layout
* **SFTP & Develop Mode:** /layouts/events/detail.html

### Tags

Tag | Description
-------------- | -------------
`{tag_addtofavorites,addtoImage,removefromImage}` | Add event to favorites list. Optionally customize to display your own custom image for adding and removing.
`{tag_body}` | Details of event (editor content)
`{tag_bookingday}` | Day of Event; for example, 12 if event date 12-Dec-2007
`{tag_bookingmonth}` | Month of event; for example, Dec if event date 12-Dec-2007
`{tag_bookingmonthnumeric}` | Month part of the date of the event as a numeric value; for example, 11-Dec07 renders 12
`{tag_bookingyear}` | Year of event; for example, 2007 if event date 12-Dec-2007
`{tag_capacity}` | Total number of seats for event
`{tag_capacitydescription}` | Description for number of seats available. Values include: Available, Filling Up, Almost Full, and Full
`{tag_capacityempty}` | Number of available seats left for event
`{tag_classifications}` | ist of categories that this event is classified under
`{tag_date}` | Date of event
`{tag_day}` | Day of event; for example, Monday, Tuesday, or Wednesday
`{tag_lastupdatedate}` | Date and time the event was last updated
`{tag_name}` | Event name
`{tag_percentfull}` | Percentage of event seats already booked
`{tag_tellafriend}` | Tell a friend about this event
