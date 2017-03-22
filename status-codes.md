---
title: "HTTP Status Codes"
layout: api
---

<table class="ui celled striped table">
	<thead>
		<tr>
			<th>Code</th>
			<th>Status</th>
			<th>Description</th>
		</tr>
	</thead>
	<tr>
		<td>200</td>
		<td>OK</td>
		<td>The request was processed and returned successfully. Nothing was changed.</td>
	</tr>
	<tr>
		<td>201</td>
		<td>Created</td>
		<td>The new resource was created successfully</td>
	</tr>
	<tr>
		<td>202</td>
		<td>Accepted</td>
		<td>The request has been accepted for processing, but the processing has not been completed. The request might or might not eventually be acted upon, as it might be disallowed when processing actually takes place.</td>
	</tr>
	<tr>
		<td>204</td>
		<td>No Content</td>
		<td>The server has fulfilled the request but does not need to return an entity-body, and might want to return updated metainformation.</td>
	</tr>
	<tr>
		<td>400</td>
		<td>Bad Request</td>
		<td>Problem with the request, such as a missing, invalid or type mismatched parameter</td>
	</tr>
	<tr>
		<td>401</td>
		<td>Unauthorized</td>
		<td>The request did not have valid authorization credentials</td>
	</tr>
	<tr>
		<td>403</td>
		<td>Forbidden</td>
		<td>Private data you are not allowed to access, or you've hit a rate limit.</td>
	</tr>
	<tr>
		<td>404</td>
		<td>Not Found</td>
		<td>Your URL is wrong, or the requested resource doesn't exist.</td>
	</tr>
	<tr>
		<td>500</td>
		<td>Server Error</td>
		<td>We call this the "crap code" error. Basically we've got a problem on our side. If this persists please contact support. We log and review all errors but your help often helps us fix it quicker.</td>
	</tr>
	<tr>
		<td>503</td>
		<td>Service Unavailable</td>
		<td>Our API is down. Please try again. We work hard to make this rare.</td>
	</tr>
</table>