---
title: Almacenar registros en formato XML
TOCTitle: Persisting Records in XML Format
ms:assetid: 8071e244-60c7-759c-094c-152add5d72e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249545(v=office.15)
ms:contentKeyID: 48545924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4b1e22c3f85c4289520326c34c6d0c218a442a3f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485184"
---
# <a name="persisting-records-in-xml-format"></a>Almacenar registros en formato XML


**Se aplica a**: Access 2013 | Office 2013

Igual que con formato ADTG, un **conjunto de registros** persistentes en formato XML se implementa con el proveedor de persistencia de Microsoft OLE DB. Este proveedor genera un conjunto de filas de sólo avance y de sólo lectura a partir de una secuencia o un archivo XML guardado que contiene la información de esquema generada por ADO. Del mismo modo, este proveedor puede tomar un **conjunto de registros** de ADO, generar XML y guardarlo en un archivo o en cualquier objeto que implemente la interfaz COM **IStream** (de hecho, un archivo no es más que otro ejemplo de objeto que admite **IStream** ). Para las versiones 2.5 y posteriores, ADO se basa en el analizador XML de Microsoft XML (MSXML) para cargar el XML en el **conjunto de registros**; por tanto, se requiere msxml.dll. Para la versión 2.5, MSXML se incluye con Internet Explorer 5. Para la versión 2.6, MSXML se incluye con SQL Server 2000.


> [!NOTE]
> <P>[!NOTA] Existen algunas limitaciones para guardar <STRONG>conjuntos de registros</STRONG> jerárquicos (formas de datos) en formato XML. No se puede guardar en XML si el <STRONG>conjunto de registros</STRONG> jerárquico contiene actualizaciones pendientes, y no se puede guardar un <STRONG>conjunto de registros</STRONG> jerárquico parametrizado. Para obtener más información, vea <A href="hierarchical-recordsets-in-xml.md">Conjuntos de registros jerárquicos en XML</A>.</P>



La forma más sencilla de conservar datos en XML y cargarlos de nuevo a través de ADO es con los métodos **Save** y **Open**, respectivamente. El siguiente código de ejemplo de ADO muestra cómo se guardan los datos de la tabla Titles en un archivo denominado titles.sav.

```vb 
 
Dim rs as new Recordset 
Dim rs2 as new Recordset 
Dim c as new Connection 
Dim s as new Stream 
 
' Query the Titles table. 
c.Open "provider='sqloledb';data source='mydb';initial catalog='pubs';Integrated Security='SSPI'" 
rs.cursorlocation = adUseClient 
rs.Open "select * from titles", c, adOpenStatic 
 
' Save to the file in the XML format. Note that if you don't specify 
' adPersistXML, a binary format (ADTG) will be used by default. 
rs.Save "titles.sav", adPersistXML 
 
' Save the Recordset into the ADO Stream object. 
rs.save s, adPersistXML 
rs.Close 
c.Close 
 
set rs = nothing 
 
Reopen the file. 
rs.Open "titles.sav",,,,adCmdFile 
'Open the Stream back into a Recordset. 
rs2.open s 
```

ADO siempre conserva el objeto **Recordset** completo. Si solo desea conservar un subconjunto de filas del objeto **Recordset**, use el método **Filter** para reducir el número de filas o cambie la cláusula de selección. Sin embargo, debe abrir un objeto **Recordset** con un cursor de cliente (**CursorLocation** = **adUseClient**) para usar el método **Filter** para guardar un subconjunto de filas. Por ejemplo, para recuperar títulos que empiecen por la letra "b", puede aplicar un filtro a un objeto **Recordset** abierto:

```vb 
 
rs.Filter "title_id like 'B*'" 
rs.Save "btitles.sav", adPersistXML 
```

ADO siempre usa el conjunto de filas de Client Cursor Engine para producir un objeto **Recordset** que permita desplazamientos y en el que se puedan establecer marcadores, además de los datos de sólo avance generados por el proveedor de persistencia.

