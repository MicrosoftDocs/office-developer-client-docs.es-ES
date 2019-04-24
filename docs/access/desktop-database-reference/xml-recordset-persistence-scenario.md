---
title: Escenario de persistencia del conjunto de registros XML
TOCTitle: XML Recordset persistence scenario
ms:assetid: 08f464da-10ba-b649-7571-766a40da2e04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248825(v=office.15)
ms:contentKeyID: 48543107
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5bae48f3e9b2b5c3967b955c41ba01c634546164
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302599"
---
# <a name="xml-recordset-persistence-scenario"></a>Escenario de persistencia del conjunto de registros XML

**Se aplica a:** Access 2013, Office 2013

En este escenario, creará una aplicación de páginas ASP que guarda el contenido de un objeto **Recordset** directamente en el objeto **Response** de ASP.

> [!NOTE]
> Este escenario requiere que el servidor tenga instalado Internet Information Server 5.0 (IIS) o una versión posterior.

El objeto **Recordset** devuelto se muestra en Internet Explorer mediante un [RDS.DataControl](datacontrol-object-rds.md).

Para crear el escenario, siga estos pasos:

1.  Configurar la aplicación.
2.  Obtener los datos.
3.  Enviar los datos.
4.  Recibir y mostrar los datos.

## <a name="step-1-set-up-the-application"></a>Paso 1: configurar la aplicación

1. Cree un directorio virtual de IIS denominado **XMLPersist** con script Permissions. 

2. Cree dos nuevos archivos de texto en la carpeta a la que señala el directorio virtual, uno denominado **XMLResponse. asp**y el otro denominado **default. htm**.


## <a name="step-2-get-the-data"></a>Paso 2: obtener los datos

En este paso, escribirá el código para abrir un objeto **Recordset** de ADO y prepararlo para su envío al cliente. 

1. Abra el archivo XMLResponse.asp con un editor de texto, tal como el Bloc de notas de Windows, e inserte el código siguiente:

   ```vb 
        
        <%@ language="VBScript" %> 
        
        <!-- #include file='adovbs.inc' --> 
        
        <% 
        Dim strSQL, strCon 
        Dim adoRec  
        Dim adoCon  
        Dim xmlDoc  
        
        ' You will need to change "slqServer" below to the name of the SQL  
        ' server machine to which you want to connect. 
        strCon = "Provider=sqloledb;Data Source=sqlServer;Initial Catalog=Pubs;Integrated Security=SSPI;" 
        Set adoCon = server.createObject("ADODB.Connection") 
        adoCon.Open strCon 
        
        strSQL = "SELECT Title, Price FROM Titles ORDER BY Price" 
        Set adoRec = Server.CreateObject("ADODB.Recordset") 
        adoRec.Open strSQL, adoCon, adOpenStatic, adLockOptimistic, adCmdText 
   ```

2. Asegúrese de cambiar el valor del parámetro de origen de datos en strCon por el nombre de su equipo con Microsoft SQL Server.

3. Mantenga el archivo abierto y vaya al paso siguiente.

## <a name="step-3-send-the-data"></a>Paso 3: enviar los datos

Ahora que ya tiene un **Recordset**, deberá enviarlo al cliente guardándolo como XML en el objeto **Response**. 

1. Agregue el código siguiente al final de XMLResponse.asp:

   ```vb 
    
    Response.ContentType = "text/xml" 
    Response.Expires = 0 
    Response.Buffer = False 
    
    
    Response.Write "<?xml version='1.0'?>" & vbNewLine 
    adoRec.save Response, adPersistXML 
    adoRec.Close 
    Set adoRec=Nothing 
    %> 
   ```

   Observe que el objeto **Response** de ASP se especifica como destino del método [Save](save-method-ado.md) del **objeto Recordset** . El destino del método **Save** puede ser cualquier objeto que admita la interfaz **IStream**, tal como un objeto ADO [Stream](stream-object-ado.md) o un nombre de archivo que incluya la ruta de acceso completa donde se va a guardar el objeto **Recordset**.

2. Antes de ir al paso siguiente, guarde y cierre XMLResponse.asp. Copie también el archivo adovbs. Inc de la carpeta\\C:\\archivos de\\programa\\archivos comunes del sistema ADO a la misma carpeta en la que tiene el archivo XMLResponse. asp.

## <a name="step-4-receive-and-display-the-data"></a>Paso 4: recibir y mostrar los datos

En este paso, se creará un archivo HTML con un [objeto RDS. DataControl](datacontrol-object-rds.md) que apunta al archivo XMLResponse. asp para obtener el objeto **Recordset**. 

1. Abra default. htm con un editor de texto, como el Bloc de notas de Windows, y agregue el código siguiente. Sustituya "sqlserver" en la dirección URL por el nombre de su equipo servidor.

   ```html 
    
    <HTML> 
    <HEAD><TITLE>ADO Recordset Persistence Sample</TITLE></HEAD> 
    <BODY> 
    
    <TABLE DATASRC="#RDC1" border="1"> 
    <TR> 
    <TD><SPAN DATAFLD="title"></SPAN></TD> 
    <TD><SPAN DATAFLD="price"></SPAN></TD> 
    </TR> 
    </TABLE> 

    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="RDC1"> 
    <PARAM NAME="URL" VALUE="XMLResponse.asp"> 
    </OBJECT> 
    
    </BODY> 
    </HTML> 
   ```

2. Cierre el archivo default.htm y guárdelo en la misma carpeta donde guardó XMLResponse.asp. 

3. Con Internet Explorer 4,0 o versiones posteriores, abra la `https://<sqlserver>/XMLPersist/default.htm` dirección URL y observe los resultados. Los datos se muestran en una tabla DHTML enlazada. 

4. Ahora, abra la `https://<sqlserver>/XMLPersist/XMLResponse.asp` dirección URL y observe los resultados. Aparecerá el XML.




