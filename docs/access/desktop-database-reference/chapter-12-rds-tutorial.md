---
title: 'Capítulo 12: tutorial del servicio de datos remotos (RDS)'
TOCTitle: 'Chapter 12: RDS tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aca77ac08688e643327bdbf229ab6c1dec40d109
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296482"
---
# <a name="chapter-12-remote-data-service-rds-tutorial"></a>Capítulo 12: tutorial del servicio de datos remotos (RDS)

**Se aplica a:** Access 2013, Office 2013

Este tutorial muestra el uso del modelo de programación RDS para consultar y actualizar un origen de datos. Primero, describe los pasos necesarios para realizar esta tarea. A continuación, el tutorial se repite en Microsoft Visual Basic Scripting Edition y Microsoft Visual J++, que incluye ADO para Windows Foundation Classes (ADO/WFC).

Este tutorial se codifica en diferentes lenguajes por dos motivos:

- La documentación para RDS supone que el lector codifica en Visual Basic. Esto hace que la documentación sea más apropiada para programadores de Visual Basic, pero menos útil para los que utilizan otros lenguajes.

- Si no está seguro de una determinada función de RDS y conoce algo de otro lenguaje, podría resolver sus dudas buscando la misma característica expresada en el otro lenguaje.

Este tutorial se basa en el modelo de programación RDS. Analiza individualmente cada paso del modelo de programación. Además, ilustra cada paso con un fragmento de código de Visual Basic.

El ejemplo de código se repite en otros lenguajes con una mínima descripción. Cada paso de un tutorial de un lenguaje de programación dado está marcado con el paso correspondiente del tutorial descriptivo y del modelo de programación. Utilice el número del paso como referencia a la explicación del tutorial descriptivo.

El modelo de programación RDS se especifica a continuación. Úselo como una guía mientras avanza en el tutorial.

### <a name="rds-programming-model-with-objects"></a>Modelo de programación de RDS con objetos

- Especifique el programa que se va a invocar en el servidor y obtenga una forma (proxy) de hacer referencia al mismo desde el cliente.

- Llame al programa de servidor. Pásele los parámetros que identifican el origen de datos y el comando que se desea emitir.

- Normalmente, el programa de servidor obtiene un objeto [Recordset](recordset-object-ado.md) desde el origen de datos utilizando ADO. Opcionalmente, el objeto **Recordset** se procesa en el servidor.

- El programa de servidor devuelve el objeto **Recordset** final a la aplicación cliente.

- En el cliente, el objeto **Recordset** se coloca opcionalmente en un formulario que se puede usar fácilmente mediante controles visuales.

- Los cambios realizados en el objeto **Recordset** se envían al servidor y se usan para actualizar el origen de datos.

## <a name="step-1-specify-a-server-program"></a>Paso 1: especificar un programa de servidor

En el caso más general, use el método [CreateObject](createobject-method-rds.md) del objeto [RDS.DataSpace](dataspace-object-rds.md) para especificar el programa predeterminado de servidor, [RDSServer.DataFactory](datafactory-object-rdsserver.md), o su propio programa de servidor personalizado (objeto de negocio). Se crea entonces una instancia del programa de servidor en el servidor y se devuelve una referencia (o *proxy*) al programa de servidor.

Este tutorial utiliza el programa de servidor predeterminado:

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
``` 

## <a name="step-2-invoke-the-server-program"></a>Paso 2: invocar el programa de servidor 

Cuando se llama a un método en el *proxy* cliente, el programa real en el servidor ejecuta el método. En este paso, se ejecutará una consulta en el servidor.

### <a name="part-a"></a>Parte A 

Si no utilizo [RDSServer.DataFactory](datafactory-object-rdsserver.md) en este tutorial, la forma más cómoda de realizar este paso sería utilizar el objeto [RDS.DataControl](datacontrol-object-rds.md). El objeto **RDS.DataControl** combina el paso anterior de crear un proxy con este paso que emite la consulta.

1. Establezca el **objeto RDS. DataControl** para identificar [](server-property-rds.md) dónde se debe crear una instancia del programa de servidor.

2. Establezca la propiedad [Connect](connect-property-rds.md) para especificar la cadena de conexión para obtener acceso al origen de datos.

3. Establezca la propiedad [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) para especificar el texto del comando de consulta. 

4. Emita el método [Refresh](refresh-method-rds.md) para hacer que el programa de servidor se conecte al origen de datos, recupere las filas especificadas en la consulta y devuelva un objeto **Recordset** al cliente.

Este tutorial no utiliza el objeto **RDS.DataControl**, pero, en caso de utilizarlo, sería del siguiente modo:

```vb 
 
Sub RDSTutorial2A() 
 Dim DC as New RDS.DataControl 
 DC.Server = "https://yourServer" 
 DC.Connect = "DSN=Pubs" 
 DC.SQL = "SELECT * FROM Authors" 
 DC.Refresh 
... 
```

<br/>

El tutorial tampoco llama a RDS con objetos de ADO, pero, en caso de hacerlo, sería del siguiente modo:

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

### <a name="part-b"></a>Parte B 

El método general para realizar este paso consiste en llamar al método [Query](query-method-rds.md) del objeto **RDSServer.DataFactory**. Ese método toma una cadena de conexión, que se utiliza para conectar con un origen de datos, y un texto de comando, utilizado para especificar las filas devueltas desde el origen de datos.

Este tutorial utiliza el método **Query** del objeto **DataFactory**:

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-3-server-obtains-a-recordset"></a>Paso 3: el servidor obtiene un conjunto de registros 

El programa servidor usa el texto del comando y la cadena de conexión para solicitar al origen de datos las filas deseadas. Normalmente, se utiliza ADO para recuperar este objeto **Recordset**, aunque también se podrían usar otras interfaces de acceso a datos de Microsoft, tales como OLE DB.

El aspecto de un programa servidor personalizado puede ser el siguiente:

```vb 
 
Public Function ServerProgram(cn as String, qry as String) as Object 
Dim rs as New ADODB.Recordset 
 rs.CursorLocation = adUseClient 
 rs.Open qry, cn 
 rs.ActiveConnection = Nothing 
 Set ServerProgram = rs 
End Function 
```

## <a name="step-4-server-returns-the-recordset"></a>Paso 4: el servidor devuelve el conjunto de registros 

RDS convierte el objeto **Recordset** recuperado en un formulario que se puede devolver al cliente (es decir, *reorganiza* el objeto **Recordset**). La forma exacta de la conversión y de cómo se envía depende de si el servidor está en Internet o en una intranet, en una red de área local, o de si se trata de una biblioteca de vínculos dinámicos (dll). No obstante, este detalle no es crítico: lo que importa es que RDS devuelva el objeto **Recordset** al cliente.

En el cliente, se recibe un objeto **Recordset** y se asigna a una variable local.

```vb 
 
Sub RDSTutorial4() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-5-datacontrol-is-made-usable"></a>Paso 5: se puede usar DataControl 

El objeto **Recordset** devuelto está disponible para su uso. Puede examinarlo, navegar por él o editarlo como lo haría con cualquier otro objeto **Recordset**. Las operaciones que se pueden realizar con **Recordset** dependen del entorno disponible. Visual Basic y Visual C++ poseen controles visuales que pueden usar un objeto **Recordset** directa o indirectamente con la ayuda de un control de datos.

Por ejemplo, si va a mostrar una página web en Internet Explorer, es posible que desee mostrar los datos del objeto **Recordset** en un control visual. Los controles visuales de una página web no pueden tener acceso directamente a un objeto **Recordset** . Sin embargo, pueden obtener acceso al objeto **Recordset** por medio del objeto [RDS.DataControl](datacontrol-object-rds.md). El **RDS.DataControl** puede ser utilizado por un control visual cuando su propiedad [SourceRecordset](recordset-sourcerecordset-properties-rds.md) se establece en el objeto **Recordset**.

El objeto control visual debe tener su parámetro **DATASRC** establecido con el valor del **RDS.DataControl**, y su propiedad **DATAFLD** con el valor de un campo (columna) del objeto **Recordset**.

En este tutorial, establezca la propiedad **SourceRecordset**:

```vb 
 
Sub RDSTutorial5() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DC as New RDS.DataControl 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
 DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
... 
```

## <a name="step-6-changes-are-sent-to-the-server"></a>Paso 6: los cambios se envían al servidor

Si se modifica el objeto **Recordset**, cualquier cambio (es decir, filas que se agregan, modifican o eliminan) se puede enviar de nuevo al servidor.

The default behavior of RDS can be invoked implicitly with ADO objects and the Microsoft OLE DB Remoting Provider. Las consultas pueden devolver **conjuntos de registros**y los **Recordsets** editados pueden actualizar el origen de datos. Este tutorial no usa RDS con objetos ADO, pero, en caso de hacerlo, sería del siguiente modo:

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

### <a name="part-a"></a>Parte A 

Suponga para este caso que solo usó el [RDS.DataControl](datacontrol-object-rds.md) y que existe ahora un objeto **Recordset** asociado con el **RDS.DataControl**. El método [SubmitChanges](submitchanges-method-rds.md) actualiza el origen de datos con los cambios del objeto **Recordset** si las propiedades [Server](server-property-rds.md) y [Connect](connect-property-rds.md) están establecidas.

```vb 
 
Sub RDSTutorial6A() 
Dim DC as New RDS.DataControl 
Dim RS as ADODB.Recordset 
DC.Server = "https://yourServer" 
DC.Connect = "DSN=Pubs" 
DC.SQL = "SELECT * FROM Authors" 
DC.Refresh 
... 
Set RS = DC.Recordset 
 ' Edit the Recordset. 
... 
DC.SubmitChanges 
... 
```

### <a name="part-b"></a>Parte B 

Como alternativa, podría actualizar el servidor con el objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md), especificando una conexión y un objeto **Recordset**.

```vb 
 
Sub RDSTutorial6B() 
Dim DS As New RDS.DataSpace 
Dim RS As ADODB.Recordset 
Dim DC As New RDS.DataControl 
Dim DF As Object 
Dim blnStatus As Boolean 
Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
 ' Edit the Recordset. 
blnStatus = DF.SubmitChanges "DSN=Pubs", RS 
End Sub 
```


## <a name="appendix-a-rds-tutorial-vbscript"></a>Apéndice A: tutorial de RDS (VBScript)

Este es el tutorial de RDS, escrito en Microsoft Visual Basic Scripting Edition. Para obtener una descripción del propósito de este tutorial, vea la introducción a este tema.

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

### <a name="step-1-specify-a-server-program"></a>Paso 1: especificar un programa de servidor

VBScript puede descubrir el nombre del servidor Web de IIS en el que se está ejecutando mediante el método **request. ServerVariables** de VBScript disponible para las páginas Active Server:

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

Sin embargo, para este tutorial, use el servidor imaginario, "yourServer".

> [!NOTE]
> [!NOTA] Preste atención a los tipos de datos de argumentos **ByRef**. VBScript no permite especificar el tipo de variable, por lo que siempre se debe pasar un tipo Variant. Cuando se usa HTTP, RDS permitirá pasar un valor Variant a un método que espera un valor no Variant si lo llama con el método **CreateObject** del objeto [RDS.DataSpace](createobject-method-rds.md). Cuando se usa DCOM o un servidor en proceso, use los mismos tipos de parámetro en el cliente y en el servidor o recibirá un error de no coincidencia de tipos.

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

### <a name="step-2-part-a-invoke-the-server-program-with-rdsdatacontrol"></a>Paso 2, parte A: invocar el programa de servidor con RDS. DataControl

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

Vaya al paso siguiente.

### <a name="step-4-server-returns-the-recordset"></a>Paso 4: el servidor devuelve el conjunto de registros

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

### <a name="step-5-datacontrol-is-made-usable-by-visual-controls"></a>Paso 5: el uso de DataControl se hace útil mediante controles visuales

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

### <a name="step-6-part-a-changes-are-sent-to-the-server-with-rdsdatacontrol"></a>Paso 6, parte A: los cambios se envían al servidor con RDS. DataControl

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

### <a name="step-6-part-b-changes-are-sent-to-the-server-with-rdsserverdatafactory"></a>Paso 6, parte B: los cambios se envían al servidor con RDSServer. DataFactory

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

## <a name="appendix-b-rds-tutorial-visual-j"></a>Apéndice B: tutorial de RDS (Visual J++)

ADO/WFC no sigue completamente el modelo de objetos RDS, ya que no implementa el objeto [RDS.DataControl](datacontrol-object-rds.md). ADO/WFC sólo implementa la clase de la parte cliente, [RDS.DataSpace](dataspace-object-rds.md).

La clase **DataSpace** implementa un método, [CreateObject](createobject-method-rds.md), que devuelve un objeto [ObjectProxy](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/objectproxy-ado-wfc-syntax). La clase **DataSpace** también implementa la propiedad [InternetTimeout](internettimeout-property-rds.md).

La clase **ObjectProxy** implementa un método, call, que puede llamar a cualquier objeto de negocio de servidor.

```java 
 
import com.ms.wfc.data.*; 
public class RDSTutorial 
{ 
 public void tutorial() 
 { 
// Step 1: Specify a server program. 
 ObjectProxy obj = 
 DataSpace.createObject( 
 "RDSServer.DataFactory", 
 "https://YourServer"); 
 
// Step 2: Server returns a Recordset. 
 Recordset rs = (Recordset) obj.call( 
 "Query", 
 new Object[] {"DSN=Pubs;", "SELECT * FROM Authors"}); 
 
// Step 3: Changes are sent to the server. 
 ... // Edit Recordset. 
 obj.call( 
 "SubmitChanges", 
 new Object[] {"DSN=Pubs;", rs}); 
 return; 
 } 
} 
```



