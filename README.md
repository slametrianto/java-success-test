# java-success-test




private void getDropListKategori(RoutingContext context) {
	responseBody = new JsonObject();
		final JsonObject requestBody =new JsonObject(context.getBodyAsString());
		final JsonObject jsonReqColumn =requestBody.getJsonObject(Dukcapil.KEY_REQ_TABLE);
		
		responseBody = new JsonObject();
		responseBody.put(Dukcapil.KEY_REQ_TABLE, jsonReqColumn);
		responseClientSuccess(context, responseBody);	
	}
	
	
	
	///success yg betul
	
	final JsonObject principalUser = context.user().principal();
	responseBody =new JsonObject();
		
	responseClientSuccess(context, responseBody);
	responseClientError(context, responseBody);
		
