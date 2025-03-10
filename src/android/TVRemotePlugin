package org.apache.cordova.androidtv;

import android.view.KeyEvent;
import org.apache.cordova.CordovaPlugin;
import org.apache.cordova.CallbackContext;
import org.json.JSONArray;
import org.json.JSONException;

public class TVRemotePlugin extends CordovaPlugin {

    @Override
    public boolean execute(String action, JSONArray args, CallbackContext callbackContext) throws JSONException {
        if ("registerKeyEvents".equals(action)) {
            callbackContext.success("Key events registered");
            return true;
        }
        return false;
    }

    @Override
    public boolean onKeyDown(int keyCode, KeyEvent event) {
        if (keyCode == KeyEvent.KEYCODE_DPAD_LEFT) {
            webView.loadUrl("javascript:document.dispatchEvent(new KeyboardEvent('keydown', {'key': 'ArrowLeft'}));");
            return true;
        } else if (keyCode == KeyEvent.KEYCODE_DPAD_RIGHT) {
            webView.loadUrl("javascript:document.dispatchEvent(new KeyboardEvent('keydown', {'key': 'ArrowRight'}));");
            return true;
        } else if (keyCode == KeyEvent.KEYCODE_DPAD_UP) {
            webView.loadUrl("javascript:document.dispatchEvent(new KeyboardEvent('keydown', {'key': 'ArrowUp'}));");
            return true;
        } else if (keyCode == KeyEvent.KEYCODE_DPAD_DOWN) {
            webView.loadUrl("javascript:document.dispatchEvent(new KeyboardEvent('keydown', {'key': 'ArrowDown'}));");
            return true;
        } else if (keyCode == KeyEvent.KEYCODE_ENTER) {
            webView.loadUrl("javascript:document.activeElement.click();");
            return true;
        }
        return super.onKeyDown(keyCode, event);
    }
}
