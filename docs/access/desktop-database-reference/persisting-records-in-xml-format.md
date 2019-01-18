---
title: Almacenamiento de registros en formato XML
TOCTitle: Persisting records in XML format
ms:assetid: 8071e244-60c7-759c-094c-152add5d72e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249545(v=office.15)
ms:contentKeyID: 48545924
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 10a5651c74580950810211c4f71e19fc80a16a95
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714727"
---
# <a name="persisting-records-in-xml-format"></a>Almacenamiento de registros en formato XML

**Se aplica a**: Access 2013, Office 2013

Igual que con formato ADTG, un **conjunto de registros** persistentes en formato XML se implementa con el proveedor de persistencia de Microsoft OLE DB. Este proveedor genera un conjunto de filas de sólo avance y de sólo lectura a partir de una secuencia o un archivo XML guardado que contiene la información de esquema generada por ADO. Del mismo modo, este proveedor puede tomar un **conjunto de registros** de ADO, generar XML y guardarlo en un archivo o en cualquier objeto que implemente la interfaz COM **IStream** (de hecho, un archivo no es más que otro ejemplo de objeto que admite **IStream** ). Para las versiones 2.5 y posteriores, ADO se basa en el analizador XML de Microsoft XML (MSXML) para cargar el XML en el **conjunto de registros**; por tanto, se requiere msxml.dll. Para la versión 2.5, MSXML se incluye con Internet Explorer 5. Para la versión 2.6, MSXML se incluye con SQL Server 2000.

> [!NOTE]
> [!NOTA] Existen algunas limitaciones para guardar **conjuntos de registros** jerárquicos (formas de datos) en formato XML. No se puede guardar en XML si el **conjunto de registros** jerárquico contiene actualizaciones pendientes, y no se puede guardar un **conjunto de registros** jerárquico parametrizado. Para obtener más información, vea [Conjuntos de registros jerárquicos en XML](hierarchical-recordsets-in-xml.md).


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

Esta sección incluye los temas siguientes:

- [Formato de persistencia XML](xml-persistence-format.md)

- [Espacios de nombres](namespaces.md)

- [Sección de esquema](schema-section.md)

- [Sección de datos](data-section.md)

- [Conjuntos de registros jerárquicos en XML](hierarchical-recordsets-in-xml.md)

- [Propiedades dinámicas del objeto Recordset en XML](recordset-dynamic-properties-in-xml.md)

- [Transformaciones XSLT](xslt-transformations.md)

- [Al guardar en el objeto XML DOM](saving-to-the-xml-dom-object.md)

- [Consideraciones de seguridad XML](xml-security-considerations.md)

- [XML Recordset Persistence Scenario Topics](xml-recordset-persistence-scenario.md)
