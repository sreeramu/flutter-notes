Just usefull notes
List<String> data = List<String>();
      data.add("value");
      var ioRequest = await _inner.openUrl(request.method, request.url);
      InstanceMirror cheaders = reflect(ioRequest.headers);
      var s = MirrorSystem.getSymbol('_headers', cheaders.type.owner);
      InstanceMirror tt = cheaders.getField(s);
      (tt.reflectee as HashMap)["dart111CCCCCCDDDDFFF"] = data;
      //tt.invoke(#putIfAbsent, ["dart111CCCCCCDDDDFFF", () => data]);

  void iset(String name,Object value){
    _headers.remove(name);
    _addValue(name, value);
  }
