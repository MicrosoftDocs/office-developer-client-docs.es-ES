---
title: Método Connection.CreateQueryDef (DAO)
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
localization_priority: Normal
ms.openlocfilehash: b6600d4508a33a31098d6a2e7c92f5904beb0e95
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295936"
---
# <a name="connectioncreatequerydef-method-dao"></a>Método Connection.CreateQueryDef (DAO)

**Se aplica a:** Access 2013, Office 2013

Crea un nuevo objeto **[QueryDef](querydef-object-dao.md)**.

## <a name="syntax"></a>Sintaxis

*expression* .CreateQueryDef(***Name***, ***SQLText***)

*expression* Variable que representa un objeto **Connection**.

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

QueryDef

## <a name="remarks"></a>Comentarios

En un área de trabajo de Microsoft Access, si proporciona cualquier otro elemento que no sea una cadena de longitud cero para el nombre al crear un objeto **QueryDef**, el objeto **QueryDef** resultante se agrega automáticamente a la colección **[QueryDefs](querydefs-collection-dao.md)**.

Si el objeto especificado por el nombre ya es un miembro de la colección **QueryDefs**, se produce un error en tiempo de ejecución. Puede crear un archivo **QueryDef** temporal utilizando una cadena de longitud cero para el argumento de nombre cuando ejecuta el método **CreateQueryDef**. También puede realizar esto estableciendo la propiedad **[nombre](connection-name-property-dao.md)** de un **QueryDef** recién creado en una cadena de longitud cero (""). Los objetos **QueryDef** temporales son útiles si quiere utilizar instrucciones SQL repetidamente sin tener que crear nuevos objetos permanentes en la colección **QueryDefs**. No puede anexar un **QueryDef** temporal a cualquier colección ya que una cadena de longitud cero no es un nombre válido para un objeto **QueryDef** permanente. Siempre puede establecer las propiedades **Name** y **SQL** del objeto **QueryDef** recién creado y posteriormente anexar **QueryDef** a la colección **QueryDefs**.

Para ejecutar una instrucción SQL en un objeto **QueryDef**, use el método **[Execute](connection-execute-method-dao.md)** u **[OpenRecordset](connection-openrecordset-method-dao.md)**.

El uso de un objeto **QueryDef** es el método recomendado para realizar consultas de paso a través SQL con bases de datos ODBC.

Para quitar un objeto **QueryDef** de una colección **QueryDefs** de una base de datos del motor de base de datos de Microsoft Access, use el método **[Delete](fields-delete-method-dao.md)** en la colección.

