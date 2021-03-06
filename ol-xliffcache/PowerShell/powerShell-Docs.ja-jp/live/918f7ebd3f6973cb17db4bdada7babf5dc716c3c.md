# DSC 構成のヘルプの作成

>適用先: Windows PowerShell 5.0

DSC 構成では、コメント ベースのヘルプを使用できます。 ユーザーは、構成関数に `-?` を付けて呼び出すか、次を使うことで、ヘルプにアクセスできます。 
[Get-Help](https://technet.microsoft.com/en-us/library/hh849696.aspx) コマンドレット。 PowerShell のコメント ベースのヘルプについて詳しくは、次をご覧ください。 
[about_Comment_Based_Help](https://technet.microsoft.com/en-us/library/hh847834.aspx).

次の例では、2 つの構成と各構成のコメント ベースのヘルプを含むスクリプトを示します。

```powershell
<#
.SYNOPSIS
A brief description of the function or script. This keyword can be used only once for each configuration.


.DESCRIPTION
A detailed description of the function or script. This keyword can be used only once for each configuration.


.PARAMETER computername
The description of a parameter. Add a .PARAMETER keyword for each parameter in the function or script syntax.

Type the parameter name on the same line as the .PARAMETER keyword. Type the parameter description on the lines following the .PARAMETER keyword. 
Windows PowerShell interprets all text between the .PARAMETER line and the next keyword or the end of the comment block as part of the parameter description. 
The description can include paragraph breaks.

The Parameter keywords can appear in any order in the comment block, but the function or script syntax determines the order in which the parameters 
(and their descriptions) appear in help topic. To change the order, change the syntax.

.PARAMETER filePath
Provide a PARAMETER section for each parameter that your script or function accepts.

.EXAMPLE
A sample command that uses the function or script, optionally followed by sample output and a description. Repeat this keyword for each example. If you have multiple examples,
there is no need to number them. PowerShell will number the examples in help text.

.EXAMPLE
This example will be labeled "EXAMPLE 2" when help is displayed to the user.
#>

configuration HelpSample1
{
    param([string]$computername,[string]$filePath)
    File f
    {
        Contents="Hello World"
        DestinationPath = "c:\Destination.txt"
    }
}
```

## 構成のヘルプの表示

構成のヘルプを表示するには、**Get-Help** コマンドレットに関数名を付けて使うか、関数名の後に「`-?`」と入力します。 次は、前の関数を
Get-Help に渡した場合の出力です。

```powershell
PS C:\> Get-Help HelpSample1

NAME
    HelpSample1
    
SYNOPSIS
    A brief description of the function or script. This keyword can be used only once for each configuration.
    
    
SYNTAX
    HelpSample1 [[-InstanceName] <String>] [[-DependsOn] <String[]>] [[-OutputPath] <String>] [[-ConfigurationData] <Hashtable>] [[-computername] 
    <String>] [[-filePath] <String>] [<CommonParameters>]
    
    
DESCRIPTION
    A detailed description of the function or script. This keyword can be used only once for each configuration.
    

RELATED LINKS

REMARKS
    To see the examples, type: "get-help HelpSample1 -examples".
    For more information, type: "get-help HelpSample1 -detailed".
    For technical information, type: "get-help HelpSample1 -full".
```

## 参照
* [DSC 構成](configurations.md)

<!--HONumber=Apr16_HO5-->


