---
title: 'Paso 2: Inicializar el cuadro de lista principal'
TOCTitle: 'Step 2: Initialize the Main List Box'
ms:assetid: 81e4dcfd-6ee0-b5f9-9ea3-026c38c26bf0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249562(v=office.15)
ms:contentKeyID: 48545967
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3505c2726da3f2f2f01d179c97cde5a1d7b635ba
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869900"
---
# <a name="step-2-initialize-the-main-list-box"></a>Paso 2: Inicializar el cuadro de lista principal


**Se aplica a**: Access 2013, Office 2013

## <a name="step-2-initialize-the-main-list-box"></a>Paso 2: Inicializar el cuadro de lista principal

**Para declarar objetos Record y Recordset globales**

  - Inserte el código siguiente en la sección de declaraciones generales de Form1:
    
    ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
    ```
    
    Este código declara referencias de objetos globales para **Record** y **Recordset** que se usarán posteriormente en este escenario.

**Para conectar con una dirección URL y llenar lstMain**

  - Inserte el código siguiente en el controlador del evento Form Load para Form1:
    
    ```vb 
     
    Private Sub Form_Load() 
        Set grec = New Record 
        Set grs = New Recordset 
        grec.Open "", "URL=https://servername/foldername/", , _ 
            adOpenIfExists Or adCreateCollection 
        Set grs = grec.GetChildren 
        While Not grs.EOF 
            lstMain.AddItem grs(0) 
            grs.MoveNext 
        Wend 
    End Sub 
    ```
    
    Este código crea instancias de los objetos globales **Record** y **Recordset**. El **registro**, grec, se abre con una dirección URL especificada como **ActiveConnection**. Si la dirección URL existe, se abre; si aún no existe, se crea. Tenga en cuenta que deberá reemplazar "https://servername/foldername/" con una dirección URL válida de su entorno. El **objeto Recordset**, grs, se abre sobre los elementos secundarios del **Record**, grec. A continuación, lstMain se rellena con los nombres de archivo de los recursos publicados en la dirección URL.

