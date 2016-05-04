---
title: Verwenden des Konsolenbereichs in der Windows PowerShell ISE
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 44d67705-87c7-4a69-a53e-6471fdebb757
---
# Verwenden des Konsolenbereichs in der Windows PowerShell ISE
Der Konsolenbereich in der [!INCLUDE[ise_1](../Token/ise_1_md.md)] funktioniert exakt so wie das eigenständige [!INCLUDE[ise_2](../Token/ise_2_md.md)]-Konsolenfenster.

Um einen Befehl im Konsolenbereich ausführen, geben Sie einen Befehl ein, und drücken Sie dann die EINGABETASTE. Um mehrere Befehle einzugeben, die nacheinander ausgeführt werden sollen, drücken Sie UMSCHALT+EINGABETASTE zwischen den Befehlen. Hilfe zum Eingeben von Befehlen finden Sie unter [Verwenden von Vervollständigung mit der TAB-TASTE im Skriptbereich und Konsolenbereich](../Topic/How-to-Use-Tab-Completion-in-the-Script-Pane-and-Console-Pane.md).

Um einen Befehl zu beenden, klicken Sie auf der Symbolleiste auf **Vorgang beenden**, oder drücken Sie STRG+UNTBR. Sie können auch STRG+C verwenden, um einen Befehl zu beenden, sofern der Kontext eindeutig ist. Wenn im aktuellen Bereich beispielsweise Text ausgewählt ist,wird STRG+C dem Kopiervorgang zugeordnet.

Seit [!INCLUDE[wps_2](../Token/wps_2_md.md)] Version 3 ist der Ausgabebereich mit dem Konsolenbereich kombiniert. Dies hat den Vorteil, dass sich das System wie die eigenständige [!INCLUDE[wps_2](../Token/wps_2_md.md)]-Konsole verhält, und beseitigt die Unterschiede in den Vorgehensweisen, die erforderlich waren, als die Bereiche getrennt waren. Sie haben folgende Möglichkeiten:

-   Markieren von Text im Konsolenbereich und Kopieren des markierten Texts in die Zwischenablage, um ihn in einem anderen Fenster einzufügen. Um Text zu markieren, ziehen Sie mit der Maus bei gedrückter linker Maustaste über den Text, den Sie erfassen möchten. Sie können Text auch markieren, indem Sie bei gedrückter **UMSCHALTTASTE** die Cursortasten verwenden. Drücken Sie dann STRG+C, oder klicken Sie auf der Symbolleiste auf das **Kopieren**-Symbol.

-   Einfügen des markierten Texts an der aktuellen Cursorposition. Klicken Sie auf der Symbolleiste auf das **Einfügen**-Symbol.

-   Löschen des gesamten Texts im Konsolenbereich. Um den Text im Konsolenbereich zu löschen, können Sie auf der Symbolleiste auf das **Konsolenbereich löschen**-Symbol klicken, oder führen Sie den Befehl **Clear-Host** oder dessen Alias **cls** aus.

## Weitere Informationen
[Verwenden der Windows PowerShell ISE](../Topic/Using-the-Windows-PowerShell-ISE.md)



<!--HONumber=Apr16_HO1-->


