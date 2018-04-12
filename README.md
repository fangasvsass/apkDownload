# apkDownload
    Uri uri = Uri.parse("letote://letote/"+miPushMessage.getExtra().get("uri"));
    Intent intent = new Intent(Intent.ACTION_VIEW, uri);
    intent.addFlags(Intent.FLAG_ACTIVITY_NEW_TASK);
    context.startActivity(intent);
    MIPushPackage.sMiPushMessage = miPushMessage;
    if (MIPushPackage.sReactContext != null) {
      sendListener("xmpush_click", miPushMessage);
