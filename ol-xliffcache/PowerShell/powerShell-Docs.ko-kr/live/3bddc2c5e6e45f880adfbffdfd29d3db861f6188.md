---
title: ISEAddOnTool 개체
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ce84d8bc-07ba-41f6-bdde-d6f3fddcd1e3
---
# ISEAddOnTool 개체
  **ISEAddonTool** 개체는 Windows PowerShell ISE에 추가적인 기능을 제공하는 설치된 추가 기능 도구를 나타냅니다. 예제는 **보기**를 클릭한 다음, **명령 추가 기능 표시**를 클릭하여 표시할 수 있는 **명령** 도구입니다. 그런 다음 사용 가능한 다양한 **ISEAddOnTool** 개체를 조작하여 이 도구에 액세스할 수 있습니다.

 각 추가 기능 도구는 세로 창이나 가로 창과 연결할 수 있습니다. 세로 창은 Windows PowerShell ISE의 오른쪽 가장자리에 도킹됩니다. 가로 창은 아래쪽 가장자리에 도킹됩니다.

 Windows PowerShell ISE의 각 PowerShell 탭에는 자체의 추가 기능 도구가 설치되어 있을 수 있습니다. [$psISE.PowerShellTabs](The-PowerShellTabCollection-Object.md) 컬렉션 개체에 있는 **PowerShellTab** 개체에서 현재 선택한 탭이나 동일한 속성에 사용할 수 있는 도구 컬렉션에 액세스하려면 [$psISE.CurrentPowerShellTab.HorizontalAddOnTools](The-ISEAddOnToolCollection-Object.md) 및 [$psISE.CurrentPowerShellTab.VerticalAddOnTools](The-ISEAddOnToolCollection-Object.md)를 참조하세요.

## 메서드
 이 클래스의 개체에 사용할 수 있는 Windows PowerShell ISE 관련 메서드는 없습니다.

## 속성

###  <a name="Control"></a> 컨트롤
  Windows PowerShell ISE 3.0 이상에서 지원되며, 이전 버전에는 없습니다.

 **컨트롤** 속성은 명령 추가 기능 도구의 세부 정보 중 많은 부분에 대한 읽기 권한을 제공합니다.

```
# View the properties of the Commands add-on tool.
# (assumes that it is visible in the vertical pane)
$psISE.CurrentVisibleVerticalTool.Control
HostObject                  : Microsoft.PowerShell.Host.ISE.ObjectModelRoot
Content                     :
HasContent                  :
ContentTemplate             :
ContentTemplateSelector     :
ContentStringFormat         :
BorderBrush                 :
BorderThickness             :
Background                  :
Foreground                  :
FontFamily                  :
FontSize                    :
FontStretch                 :
FontStyle                   :
FontWeight                  :
HorizontalContentAlignment  :
VerticalContentAlignment    :
TabIndex                    :
IsTabStop                   :
Padding                     :
Template                    : System.Windows.Controls.ControlTemplate
Style                       :
OverridesDefaultStyle       :
UseLayoutRounding           :
Triggers                    : {}
TemplatedParent             :
Resources                   : {System.Windows.Controls.TabItem}
DataContext                 :
BindingGroup                :
Language                    :
Name                        :
Tag                         :
InputScope                  :
ActualWidth                 : 370.75
ActualHeight                : 676.559097412109
LayoutTransform             :
Width                       :
MinWidth                    :
MaxWidth                    :
Height                      :
MinHeight                   :
MaxHeight                   :
FlowDirection               : LeftToRight
Margin                      :
HorizontalAlignment         :
VerticalAlignment           :
FocusVisualStyle            :
Cursor                      :
ForceCursor                 :
IsInitialized               : True
IsLoaded                    :
ToolTip                     :
ContextMenu                 :
Parent                      :
HasAnimatedProperties       :
InputBindings               :
CommandBindings             :
AllowDrop                   :
DesiredSize                 : 227.66,676.559097412109
IsMeasureValid              : True
IsArrangeValid              : True
RenderSize                  : 370.75,676.559097412109
RenderTransform             :
RenderTransformOrigin       :
IsMouseDirectlyOver         : False
IsMouseOver                 : False
IsStylusOver                : False
IsKeyboardFocusWithin       : False
IsMouseCaptured             :
IsMouseCaptureWithin        : False
IsStylusDirectlyOver        : False
IsStylusCaptured            :
IsStylusCaptureWithin       : False
IsKeyboardFocused           : False
IsInputMethodEnabled        :
Opacity                     :
OpacityMask                 :
BitmapEffect                :
Effect                      :
BitmapEffectInput           :
CacheMode                   :
Uid                         :
Visibility                  : Visible
ClipToBounds                : False
Clip                        :
SnapsToDevicePixels         : False
IsFocused                   :
IsEnabled                   :
IsHitTestVisible            :
IsVisible                   : True
Focusable                   :
PersistId                   : 1
IsManipulationEnabled       :
AreAnyTouchesOver           : False
AreAnyTouchesDirectlyOver   :
AreAnyTouchesCapturedWithin : False
AreAnyTouchesCaptured       :
TouchesCaptured             : {}
TouchesCapturedWithin       : {}
TouchesOver                 : {}
TouchesDirectlyOver         : {}
DependencyObjectType        : System.Windows.DependencyObjectType
IsSealed                    : False
Dispatcher                  : System.Windows.Threading.Dispatcher

```

###  <a name="IsVisible"></a> IsVisible
  Windows PowerShell ISE 3.0 이상에서 지원되며, 이전 버전에는 없습니다.

 추가 기능 도구가 현재 할당된 해당 창에 표시되는지 여부를 나타내는 부울 속성입니다. 표시되는 경우, **IsVisible** 속성을 **$false**로 설정하여 도구를 숨기거나, **IsVisible** 속성을 **$true**로 설정하여 추가 기능이 PowerShell 탭에 표시되도록 할 수 있습니다. 추가 기능 도구가 숨겨지면 더 이상 **CurrentVisibleHorizontalTool** 또는 **CurrentVisibleVerticalTool** 개체를 통해 액세스할 수 없으며, 따라서 해당 개체에서 이 속성을 사용하여 표시할 수 없습니다.

```
# Hide the current tool in the vertical tool pane
$psISE.CurrentVisibleVerticalTool.IsVisible = $false
# Show the first tool on the currently selected PowerShell tab
$psISE.CurrentPowerShellTab.VerticalAddOnTools[0].IsVisible=$true

```

###  <a name="name"></a> 이름
  Windows PowerShell ISE 3.0 이상에서 지원되며, 이전 버전에는 없습니다.

 추가 기능 도구의 이름을 가져오는 읽기 전용 속성입니다.

```
# Gets the name of the visible vertical pane add-on tool.
$psISE.CurrentVisibleVerticalTool.name
Commands

```

## 참고 항목
 [ISEAddOnToolCollection 개체](The-ISEAddOnToolCollection-Object.md)
 [Windows PowerShell ISE 스크립팅 개체 모델](The-Windows-PowerShell-ISE-Scripting-Object-Model.md)
 [Windows PowerShell ISE 개체 모델 참조](Windows-PowerShell-ISE-Object-Model-Reference.md)
 [ISE 개체 모델 계층 구조](The-ISE-Object-Model-Hierarchy.md)


<!--HONumber=May16_HO2-->


