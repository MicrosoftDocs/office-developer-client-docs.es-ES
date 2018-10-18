---
title: Relation.CreateField Method (DAO)
TOCTitle: CreateField Method
ms:assetid: bc60c91e-acef-1c90-7303-12f77cce15b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822717(v=office.15)
ms:contentKeyID: 48547411
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8d86230f99afb95d121ea683ed4324d361b77757
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602898"
---
# <a name="relationcreatefield-method-dao"></a>Relation.CreateField Method (DAO)


**Se aplica a**: Access 2013 | Office 2013

Crea un nuevo objeto **[Field](field-object-dao.md)** (sólo áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . CreateField (***nombre***, ***tipo***, ***tamaño***)

*expresión* Variable que representa un objeto **Relation** .

### <a name="parameters"></a>Parámetros

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
<th><p>Necesario/Opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Nombre</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Una cadena que asigna nombres únicos al nuevo objeto <strong>Field</strong>. Consulte la propiedad <strong><a href="connection-name-property-dao.md">Name</a></strong> para obtener más detalles sobre los nombres de <strong>Field</strong> válidos.  </p></td>
</tr>
<tr class="even">
<td><p>Tipo</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Argumento no admitido en este objeto.</p></td>
</tr>
<tr class="odd">
<td><p>Size</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Argumento no admitido en este objeto.</p></td>
</tr>
</tbody>
</table>


<<<<<<< HEAD
### <a name="return-value"></a>Valor devuelto
=======
### <a name="return-value"></a>Valor devuelto
>>>>>>> master

Field

## <a name="remarks"></a>Observaciones

Puede utilizar el método **CreateField** para crear un nuevo campo, así como para especificar el nombre, el tipo de datos y el tamaño del campo. Si omite uno o varios de los argumentos opcionales cuando utiliza **CreateField**, puede usar la instrucción de asignación pertinente para establecer o restablecer la propiedad correspondiente antes de agregar el nuevo objeto a una colección. Después de agregar el nuevo objeto, podrá modificar algunos de sus valores, pero no todos. Vea los temas correspondientes a cada propiedad para obtener información más detallada.

Los argumentos de tipo y el tamaño se aplican sólo a objetos **Field** de un objeto **TableDef** . Estos argumentos se omiten cuando un objeto **Field** está asociado a un objeto **Index** o **Relation**.

Si name hace referencia a un objeto que ya es un miembro de la colección, se produce un error en tiempo de ejecución cuando se utiliza el método **[Append](fields-append-method-dao.md)** .

Para quitar un objeto **Field** de una colección **Fields**, utilice el método **[Delete](fields-delete-method-dao.md)** en la colección. No puede eliminar un objeto **Field** desde la colección **Fields** de un objeto **TableDef** después de crear un índice que haga referencia al campo.

