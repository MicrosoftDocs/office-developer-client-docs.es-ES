---
title: Tutorial de RDS (VBScript)
TOCTitle: RDS tutorial (VBScript)
ms:assetid: 7a6596fd-00b9-a637-7d00-fb55a621305f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249506(v=office.15)
ms:contentKeyID: 48545792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 996c0adf8c883de5c73174d726cf5bd11fc42457
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996884"
---
# <a name="rds-tutorial-vbscript"></a>Tutorial de RDS (VBScript)

**Se aplica a**: Access 2013, Office 2013

Este es el tutorial de RDS, escrito en Microsoft Visual Basic Scripting Edition. Para obtener una descripción del propósito de este tutorial, vea el [tutorial de RDS](chapter-12-rds-tutorial.md).

En este tutorial, [RDS. DataControl](datacontrol-object-rds.md) y [RDS. DataSpace](dataspace-object-rds.md) se crean en tiempo de diseño; es decir, se definen con etiquetas de objeto. De forma alternativa, se podrían crear en tiempo de ejecución con el método **Server.CreateObject**. 

Por ejemplo, el objeto **RDS.DataControl** se crearía del siguiente modo:

```vb
    Set DC = Server.CreateObject("RDS.DataControl") 
     <!-- RDS.DataControl --> 
     <OBJECT 
     ID="DC1" CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E33"> 
     </OBJECT> 
     
     <!-- RDS.DataSpace --> 
     <OBJECT 
     ID="DS1" WIDTH=1 HEIGHT=1 
     CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E36"> 
     </OBJECT> 
     
     <SCRIPT LANGUAGE="VBScript"> 
     
     Sub RDSTutorial() 
     Dim DF1 
```

## <a name="step-1--specify-a-server-program"></a>Paso 1 : Especificar un programa de servidor

VBScript puede descubrir el nombre del servidor web IIS que se está ejecutando mediante el método **Request.ServerVariables** de VBScript disponible para páginas Active Server:

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

Sin embargo, para este tutorial, utilice el servidor imaginario "yourServer".

> [!NOTE]
> [!NOTA] Preste atención a los tipos de datos de argumentos **ByRef**. VBScript no permite especificar el tipo de variable, por lo que siempre se debe pasar un tipo Variant. Cuando se usa HTTP, RDS permitirá pasar un valor Variant a un método que espera un valor no Variant si lo llama con el método **CreateObject** del objeto [RDS.DataSpace](createobject-method-rds.md). Cuando se usa DCOM o un servidor en proceso, use los mismos tipos de parámetro en el cliente y en el servidor o recibirá un error de no coincidencia de tipos.

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

## <a name="step-2a--invoke-the-server-program-with-rdsdatacontrol"></a>Paso 2a : Llamar al programa de servidor con RDS.DataControl

Este ejemplo es simplemente un comentario que muestra que el comportamiento predeterminado del objeto **RDS.DataControl** consiste en realizar la consulta especificada.

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial2A() 
 Dim RS 
 DC1.Refresh 
 Set RS = DC1.Recordset 
... 
```

## <a name="step-2b--invoke-the-server-program-with-rdsserverdatafactory"></a>Paso 2b : Llamar al programa servidor con RDSServer.DataFactory

## <a name="step-3--server-obtains-a-recordset"></a>Paso 3 : El servidor obtiene un objeto Recordset

## <a name="step-4--server-returns-the-recordset"></a>Paso 4 : El servidor devuelve un objeto Recordset

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

## <a name="step-5--datacontrol-is-made-usable-by-visual-controls"></a>Paso 5 : El uso de DataControl se facilita mediante controles visuales

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

## <a name="step-6a--changes-are-sent-to-the-server-with-rdsdatacontrol"></a>Paso 6a: los cambios se envían al servidor con RDS. DataControl *

Este ejemplo es simplemente un comentario que demuestra cómo el objeto **RDS.DataControl** realiza las actualizaciones.

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial6A() 
Dim RS 
DC1.Refresh 
... 
Set RS = DC1.Recordset 
' Edit the Recordset object... 
' The SERVER and CONNECT properties are already set from Step 2A. 
Set DC1.SourceRecordset = RS 
... 
DC1.SubmitChanges 
```

## <a name="step-6b--changes-are-sent-to-the-server-with-rdsserverdatafactory"></a>Paso 6b : Los cambios se envían al servidor con RDSServer.DataFactory

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

**Éste es el final del tutorial.**

