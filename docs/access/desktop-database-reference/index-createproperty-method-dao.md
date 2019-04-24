---
title: Método index. CreateProperty (DAO)
TOCTitle: CreateProperty Method
ms:assetid: 712bccd2-c8a8-cc96-6f77-6d93d92320d9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195775(v=office.15)
ms:contentKeyID: 48545578
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1d7fcaa959c0fa5f8d42d9b00a920e987ca2f126
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291841"
---
# <a name="indexcreateproperty-method-dao"></a>Método index. CreateProperty (DAO)

**Se aplica a:** Access 2013, Office 2013

Crea un nuevo objeto **[Property](property-object-dao.md)** definido por el usuario (sólo áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . CreateProperty (***nombre***, ***tipo***, ***valor***, ***DDL***)

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
<td><p><strong>String</strong> que identifica inequívocamente el nuevo objeto <strong>Property</strong>. Vea el tema relativo a la propiedad <strong>Name</strong> para obtener información detallada sobre los nombres de <strong>Property</strong> válidos.</p></td>
</tr>
<tr class="even">
<td><p><em>Tipo</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Constante que define el tipo de datos del nuevo objeto <strong>Property</strong>. Consulte la propiedad <strong><a href="field-type-property-dao.md">Type</a></strong> para obtener los tipos de datos válidos.</p></td>
</tr>
<tr class="odd">
<td><p><em>Value</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> que contiene el valor inicial de la propiedad. Vea la propiedad <strong><a href="field-value-property-dao.md">Value</a></strong> para obtener más detalles.</p></td>
</tr>
<tr class="even">
<td><p><em>INSTRUCCIÓN</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (subtipo <strong>Boolean</strong>) que indica si el objeto <strong>Property</strong> es un objeto DLL. El valor predeterminado es <strong>False</strong>. Si DDL es <strong>true</strong>, los usuarios no pueden cambiar o eliminar este objeto <strong>Property</strong> a menos que tengan el permiso <strong>dbSecWriteDef</strong> .</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor devuelto

Propiedad

## <a name="remarks"></a>Comentarios

Sólo puede crear un objeto **Property** definido por el usuario en la colección **[Properties](properties-collection-dao.md)** de un objeto que sea persistente.

Si omite uno o varios de los argumentos opcionales cuando utiliza **CreateProperty**, puede usar la instrucción de asignación pertinente para establecer o restablecer la propiedad correspondiente antes de agregar el nuevo objeto a una colección. Después de agregar el objeto, podrá modificar algunos de sus valores, pero no todos. Vea los temas relativos a las propiedades **Name**, **Type** y **Value** para obtener más información.

Si Name hace referencia a un objeto que ya es miembro de la colección, se produce un error en tiempo de ejecución cuando se utiliza el método **[Append](fields-append-method-dao.md)** .

Para quitar un objeto **Property** definido por el usuario de la colección, utilice el método **[Delete](fields-delete-method-dao.md)** en la colección **Properties**. No se pueden eliminar propiedades integradas.

> [!NOTE]
> Si se omite el argumento DDL, el valor predeterminado es false (no DDL). Dado que no se expone ninguna propiedad DDL correspondiente, debe eliminar y volver a crear un objeto **Property** que desee cambiar de DDL a no DDL.


