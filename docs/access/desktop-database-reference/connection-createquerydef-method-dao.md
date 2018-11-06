---
title: Connection.CreateQueryDef (método) (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 254fe81a-9b45-e8e7-108d-503c1c1c0fcc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191860(v=office.15)
ms:contentKeyID: 48543781
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053067
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 681da274ab1f709da2eb614df038e6aa492a224a
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997255"
---
# <a name="connectioncreatequerydef-method-dao"></a>Connection.CreateQueryDef (método) (DAO)

**Se aplica a**: Access 2013, Office 2013

Crea un nuevo objeto **[QueryDef](querydef-object-dao.md)**.

## <a name="syntax"></a>Sintaxis

*expresión* . CreateQueryDef (***nombre***, ***SQLText***)

*expresión* Variable que representa un objeto **Connection** .

## <a name="parameters"></a>Parámetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Obligatorio/opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (subtipo <strong>String</strong>) que designa inequívocamente el nuevo objeto <strong>QueryDef</strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>SQLText</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (subtipo <strong>String</strong>) que es una instrucción SQL que define el objeto <strong>QueryDef</strong>. Si omite este argumento, puede definir el objeto <strong>QueryDef</strong> estableciendo su propiedad <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> antes o después de agregarlo a una colección.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor devuelto

Objeto QueryDef

## <a name="remarks"></a>Observaciones

En un área de trabajo de Microsoft Access, si proporciona cualquier otro elemento que no sea una cadena de longitud cero para el nombre al crear un objeto **QueryDef**, el objeto **QueryDef** resultante se agrega automáticamente a la colección **[QueryDefs](querydefs-collection-dao.md)**.

Si el objeto especificado por el nombre ya es un miembro de la colección **QueryDefs** , se produce un error en tiempo de ejecución. Puede crear un **objeto QueryDef** de temporal utilizando una cadena de longitud cero para el argumento name cuando ejecute el método **CreateQueryDef** . También puede hacerlo estableciendo la propiedad **[Name](connection-name-property-dao.md)** de un **objeto QueryDef** de recién creado en una cadena de longitud cero (""). Los objetos **QueryDef** temporales son útiles si desea utilizar repetidamente instrucciones SQL sin tener que crear nuevos objetos permanentes en la colección **QueryDefs** . No se puede anexar un **objeto QueryDef** de temporal a cualquier colección debido a que una cadena de longitud cero no es un nombre válido para un objeto **QueryDef** permanente. Siempre puede establecer el **nombre** y las propiedades **SQL** del objeto **QueryDef** recién creado y, posteriormente, anexe el **objeto QueryDef** a la colección **QueryDefs** .

Para ejecutar una instrucción SQL en un objeto **QueryDef**, use el método **[Execute](connection-execute-method-dao.md)** u **[OpenRecordset](connection-openrecordset-method-dao.md)**.

El uso de un objeto **QueryDef** es el método recomendado para realizar consultas de paso SQL con bases de datos ODBC.

Para quitar un objeto **QueryDef** de una colección **QueryDefs** en una base de datos del motor de base de datos de Microsoft Access, utilice el método **[Delete](fields-delete-method-dao.md)** en la colección.

