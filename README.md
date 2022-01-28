# java-success-test




private void getDropListKategori(RoutingContext context) {
		final JsonObject principal = context.user().principal();
		final JsonObject requestBody = new JsonObject(context.getBodyAsString());
		final JsonObject jsonReqColumn = requestBody.getJsonObject(Dukcapil.KEY_REQ_TABLE);
		final JsonObject jsonWhere = new JsonObject();
		
		
		responseBody = new JsonObject();
		responseBody.put(Dukcapil.KEY_REQ_TABLE, jsonReqColumn);
		responseClientSuccess(context, responseBody);
	}
		
