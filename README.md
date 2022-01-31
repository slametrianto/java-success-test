# java-success-test




private void getDropListKategori(RoutingContext context) {
final JsonObject principalUser = context.user().principal();
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
	
	
	
	=> pastikan url https://127.0.1.1:3000/dafduk/rentan/skot/procTempatPendataanAdd
	
	dijava
	
	=> contoh VerticleBussinessAppClientSiakDafduk.java
	
	 => buat router 
	 
	router.mountSubRouter(prefixUrl + "/rentan/skot", getTempatPendataanAdd());
	
	private Router getTempatPendataanAdd() {
		final skot tempatPendataanAdd = new skot(getVertx());
		return tempatPendataanAdd.getSecuredRouter();
	}
	
	
	
	=> Dukcapil.java
	
	public static String URL_TEMPAT_PENDATAAN    = "/procTempatPendataanAdd";
	
	
	
	=> lalu buat class dijava bebas namanya (sesuai url di htmlny procTempatPendataanAdd)
	
	private void procTempatPendataanAdd(RoutingContext context) {
		
		final JsonObject principalUser = context.user().principal();
		
		responseBody =new JsonObject();
		
		responseClientSuccess(context, responseBody);
		responseClientError(context, responseBody);
		
