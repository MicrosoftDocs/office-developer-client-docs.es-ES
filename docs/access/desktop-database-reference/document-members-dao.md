---
title: Miembros del documento (DAO)
TOCTitle: Document Members
ms:assetid: 8de770e6-e4d1-372a-3ef8-8539c921b41f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197365(v=office.15)
ms:contentKeyID: 48546270
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cd50ec72113b0615849ff6b8b2e8d73c0e61c3ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293794"
---
# <a name="document-members-dao"></a>Miembros del documento (DAO)


**Se aplica a:** Access 2013, Office 2013

Un objeto Document incluye información sobre una instancia de un objeto. El objeto puede ser una base de datos, una tabla guardada, una consulta o una relación (sólo bases de datos del motor de base de datos de Microsoft Access).

## <a name="methods"></a>Métodos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="document-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Crea un nuevo objeto <strong><a href="property-object-dao.md">Property</a></strong> definido por el usuario (sólo áreas de trabajo de Microsoft Access).</p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a>Propiedades

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="document-container-property-dao.md">Contenedor</a></strong></p></td>
<td><p>Devuelve el nombre del objeto <strong><a href="container-object-dao.md">Container</a></strong> al que pertenece un objeto <strong>Document</strong> (solo en áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="document-datecreated-property-dao.md">DateCreated</a></strong></p></td>
<td><p>Devuelve la fecha y la hora en que se creó un objeto. <strong>Variant</strong> de sólo lectura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="document-lastupdated-property-dao.md">LastUpdated</a></strong></p></td>
<td><p>Devuelve la fecha y la hora del último cambio realizado en un objeto. <strong>Variant</strong> de sólo lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="document-name-property-dao.md">Name</a></strong></p></td>
<td><p>Devuelve el nombre del objeto especificado. Sólo lectura de la <strong>cadena</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="document-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>Devuelve la colección <strong><a href="properties-collection-dao.md">Properties</a></strong> de un objeto especificado. Sólo lectura.</p></td>
</tr>
</tbody>
</table>

