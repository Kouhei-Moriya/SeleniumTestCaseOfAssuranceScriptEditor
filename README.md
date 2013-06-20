参考文献
http://d.hatena.ne.jp/unageanu/20111031/1320016739
http://d.hatena.ne.jp/nigredo/20091104/1257341341
http://ozzy2010.blogspot.jp/2012/07/seleniumxpath.html

・変更するDcaseのIDは変更すること(deletedcaseのid=d42の42の部分など）

IDEによるテストケース作成時の問題
・指定するボタンがマウスオーバーで出現する場合、それを発見できない
（例：ゴールにマウスオーバー→「出てきた＋ボタン」にマウスオーバー→「出てきたストラテジ」をクリック→テキストボックスに入力）
「」内に記したボタンを、seleniumは発見できない
→mouseoverイベントをfireEventすることで解決
→→トップゴール以外の＋ボタンを押せない問題が発生、解決策を考える
→→→XPathを用いることで解決する

・テキストボックスが閉じない→blurのfireEventを明示的にはさむ
（新規ノード作成のテキストボックスの場合はclick css=#viewer > div）

・store命令を用いて一部の環境変数を前に置いた


selenium rcはテストスイートが必要なため共通のテストケースを1つ使用してスイートを組んでから使う
java -jar selenium-server-standalone-2.33.0.jar  -htmlSuite "*firefox" "http://www.ubicg.ynu.ac.jp/" "/home/kouhei/Developments/seleniumtestcase/seleniumIDE/xxxxx" "/home/kouhei/result"

*firefox
*googlechrome


Seleniumは実行するアプリケーションが別サーバだと実行できない？→別にそんなことない


selenium内のjavascript{}からthis.～で使用できるもの
browserbot[object] optionLocatorFactory[object] page[function] defaultTimeout[string] mouseSpeed[number] reset[function] doClick[function] doDoubleClick[function] doContextMenu[function] doClickAt[function] doDoubleClickAt[function] doContextMenuAt[function] doFireEvent[function] doFocus[function] doKeyPress[function] doShiftKeyDown[function] doShiftKeyUp[function] doMetaKeyDown[function] doMetaKeyUp[function] doAltKeyDown[function] doAltKeyUp[function] doControlKeyDown[function] doControlKeyUp[function] doKeyDown[function] doKeyUp[function] doMouseOver[function] doMouseOut[function] doMouseDown[function] doMouseDownRight[function] doMouseDownAt[function] doMouseDownRightAt[function] doMouseUp[function] doMouseUpRight[function] doMouseUpAt[function] doMouseUpRightAt[function] doMouseMove[function] doMouseMoveAt[function] doType[function] doTypeKeys[function] doSetSpeed[function] getSpeed[function] findToggleButton[function] doCheck[function] doUncheck[function] doSelect[function] doAddSelection[function] doRemoveSelection[function] doRemoveAllSelections[function] doSubmit[function] makePageLoadCondition[function] doOpen[function] doOpenWindow[function] doSelectWindow[function] doSelectPopUp[function] doDeselectPopUp[function] doSelectFrame[function] getWhetherThisFrameMatchFrameExpression[function] getWhetherThisWindowMatchWindowExpression[function] doWaitForPopUp[function] doChooseCancelOnNextConfirmation[function] doChooseOkOnNextConfirmation[function] doAnswerOnNextPrompt[function] doGoBack[function] doRefresh[function] doClose[function] ensureNoUnhandledPopups[function] isAlertPresent[function] isPromptPresent[function] isConfirmationPresent[function] getAlert[function] getConfirmation[function] getPrompt[function] getLocation[function] getTitle[function] getBodyText[function] getValue[function] getText[function] doHighlight[function] getEval[function] isChecked[function] getTable[function] getSelectedLabels[function] getSelectedLabel[function] getSelectedValues[function] getSelectedValue[function] getSelectedIndexes[function] getSelectedIndex[function] getSelectedIds[function] getSelectedId[function] isSomethingSelected[function] findSelectedOptionProperties[function] findSelectedOptionProperty[function] getSelectOptions[function] getAttribute[function] isTextPresent[function] isElementPresent[function] isVisible[function] findEffectiveStyleProperty[function] _isDisplayed[function] findEffectiveStyle[function] isEditable[function] getAllButtons[function] getAllLinks[function] getAllFields[function] getAttributeFromAllWindows[function] findWindow[function] doDragdrop[function] doSetMouseSpeed[function] getMouseSpeed[function] doDragAndDrop[function] doDragAndDropToObject[function] doWindowFocus[function] doWindowMaximize[function] getAllWindowIds[function] getAllWindowNames[function] getAllWindowTitles[function] getHtmlSource[function] doSetCursorPosition[function] getElementIndex[function] isOrdered[function] _isCommentOrEmptyTextNode[function] getElementPositionLeft[function] getElementPositionTop[function] getElementWidth[function] getElementHeight[function] getCursorPosition[function] getExpression[function] getXpathCount[function] getCssCount[function] doAssignId[function] doAllowNativeXpath[function] doIgnoreAttributesWithoutValue[function] doWaitForCondition[function] doSetTimeout[function] doWaitForPageToLoad[function] doWaitForFrameToLoad[function] _isNewPageLoaded[function] _abortXhrRequest[function] preprocessParameter[function] replaceVariables[function] getCookie[function] getCookieByName[function] isCookiePresent[function] doCreateCookie[function] doDeleteCookie[function] doDeleteAllVisibleCookies[function] doSetBrowserLogLevel[function] doRunScript[function] doAddLocationStrategy[function] doCaptureEntirePageScreenshot[function] doRollup[function] doAddScript[function] doRemoveScript[function] doUseXpathLibrary[function] doSendKeys[function] doPause[function] doBreak[function] doStore[function] XXXdoModalDialogTest[function] doEcho[function] _doSetSpeed[function] _getSpeed[function] assertSelected[function] assertFailureOnNext[function] assertErrorOnNext[function] doStoreText[function] doStoreAttribute[function]
