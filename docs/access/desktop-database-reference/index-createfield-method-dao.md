---
title: Método index. CreateField (DAO)
TOCTitle: CreateField Method
ms:assetid: fc82b785-8768-b144-a2a4-c1f1798865a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837208(v=office.15)
ms:contentKeyID: 48548892
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aedda14273446ff6823776e535eb7995aa127fa5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291834"
---
# <a name="indexcreatefield-method-dao"></a>Método index. CreateField (DAO)

**Se aplica a:** Access 2013, Office 2013

Crea un nuevo objeto **[Field](field-object-dao.md)** (sólo áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . CreateField (***nombre***, ***tipo***, ***tamaño***)

*expresión* Variable que representa un objeto **index** .

## <a name="parameters"></a>Parameters

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
<td><p>Una cadena que asigna nombres únicos al nuevo objeto <strong>Field</strong>. Consulte la propiedad <strong><a href="connection-name-property-dao.md">Name</a></strong> para obtener más detalles sobre los nombres de <strong>Field</strong> válidos.  </p></td>
</tr>
<tr class="even">
<td><p><em>Tipo</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Argumento no admitido en este objeto.</p></td>
</tr>
<tr class="odd">
<td><p><em>Size</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Argumento no admitido en este objeto.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor devuelto

Field

## <a name="remarks"></a>Comentarios

Puede usar el método **CreateField** para crear un nuevo campo, así como para especificar el nombre, el tipo de datos y el tamaño del campo. Si omite una o más partes opcionales al usar **CreateField**, puede usar una instrucción de asignación adecuada para configurar o restablecer la propiedad correspondiente antes de anexar el nuevo objeto a la colección. Tras anexar el nuevo objeto, puede modificar algunas, pero no todas, las configuraciones de la propiedad. Consulte los temas de propiedades individuales para obtener más detalles.

Los argumentos Type y size sólo se aplican a objetos **Field** en un objeto **TableDef** . Estos argumentos se omiten cuando se asocia un campo **Field** con un objeto **Index** o **Relation**.

Si Name hace referencia a un objeto que ya es miembro de la colección, se produce un error en tiempo de ejecución cuando se utiliza el método **[Append](fields-append-method-dao.md)** .

Para eliminar un objeto **Field** de una colección **Fields**, utilice el método **[Delete](fields-delete-method-dao.md)** de una colección. No puede eliminar un objeto **Field** de una colección **Fields** de un objeto **TableDef** después de crear un índice que hace referencia al campo.

