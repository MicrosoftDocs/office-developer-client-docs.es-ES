---
title: Tutorial de RDS (VBScript)
TOCTitle: RDS Tutorial (VBScript)
ms:assetid: 7a6596fd-00b9-a637-7d00-fb55a621305f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249506(v=office.15)
ms:contentKeyID: 48545792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d87dc84217b716505302464825a1857fecf67669
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606825"
---
# <a name="rds-tutorial-vbscript"></a>Tutorial de RDS (VBScript)


**Se aplica a**: Access 2013 | Office 2013

Éste es el Tutorial de RDS, escrito en Microsoft Visual Basic Scripting Edition. Para obtener una descripción del propósito de este tutorial, vea [Tutorial de RDS](chapter-12-rds-tutorial.md).

En este tutorial, [RDS. DataControl](datacontrol-object-rds.md) y [RDS. DataSpace](dataspace-object-rds.md) se crean en tiempo de diseño, es decir, se definen con etiquetas de objeto como ésta:. De forma alternativa, se podrían crear en tiempo de ejecución con el método **Server.CreateObject**. Por ejemplo, el objeto **RDS.DataControl** se crearía del siguiente modo:

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

**Paso 1 : Especificar un programa de servidor**

<<<<<<< HEAD VBScript puede descubrir el nombre del servidor Web de IIS se está ejecutando mediante el método **Request.ServerVariables** de VBScript disponible para páginas Active Server: === VBScript puede descubrir el nombre del sitio web IIS servidor que se ejecuta mediante el método **Request.ServerVariables** de VBScript disponible para páginas Active Server:
>>>>>>> master

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

Sin embargo, para este tutorial, utilice el servidor imaginario "yourServer".


> [!NOTE]
> <P>[!NOTA] Preste atención a los tipos de datos de argumentos <STRONG>ByRef</STRONG>. VBScript no permite especificar el tipo de variable, por lo que siempre se debe pasar un tipo Variant. Cuando se usa HTTP, RDS permitirá pasar un valor Variant a un método que espera un valor no Variant si lo llama con el método <STRONG>CreateObject</STRONG> del objeto <A href="createobject-method-rds.md">RDS.DataSpace</A>. Cuando se usa DCOM o un servidor en proceso, use los mismos tipos de parámetro en el cliente y en el servidor o recibirá un error de no coincidencia de tipos.</P>

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

**Paso 2a : Llamar al programa de servidor con RDS.DataControl**

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

**Paso 2b : Llamar al programa servidor con RDSServer.DataFactory**

**Paso 3 : El servidor obtiene un objeto Recordset**

**Paso 4 : El servidor devuelve un objeto Recordset**

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

**Paso 5 : El uso de DataControl se facilita mediante controles visuales**

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

**Paso 6a : Los cambios se envían al servidor con RDS.DataControl**

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

**Paso 6b : Los cambios se envían al servidor con RDSServer.DataFactory**

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

**Éste es el final del tutorial.**

