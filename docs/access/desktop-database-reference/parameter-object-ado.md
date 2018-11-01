---
title: Parameter (objeto) (ADO)
TOCTitle: Parameter Object (ADO)
ms:assetid: 7577598e-3d0c-30c6-5f24-1cfe98791798
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249481(v=office.15)
ms:contentKeyID: 48545676
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 382945e1f2ff37eb2155b2bc0db9f521ca85d2de
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878279"
---
# <a name="parameter-object-ado"></a>Parameter (objeto) (ADO)


**Se aplica a**: Access 2013, Office 2013

Representa un parámetro o un argumento asociado a un objeto [Command](command-object-ado.md) basado en una consulta parametrizada o un procedimiento almacenado.

## <a name="remarks"></a>Comentarios

Gran número de proveedores admiten comandos parametrizados. Se trata de comandos en los que la acción deseada se define una vez, pero se usan variables (o parámetros) para modificar algunos detalles del comando. Por ejemplo, una instrucción SELECT de SQL podría usar un parámetro para definir los criterios de coincidencia de una cláusula WHERE y otro parámetro para definir el nombre de columna para una cláusula SORT BY.

Los objetos **Parameter** representan parámetros asociados a consultas parametrizadas, o los argumentos de entrada/salida y los valores devueltos de procedimientos almacenados. Dependiendo de la funcionalidad del proveedor, es posible que algunas colecciones, métodos o propiedades de un objeto **Parameter** no estén disponibles.

Con las colecciones, los métodos y las propiedades de un objeto **Parameter**, se puede hacer lo siguiente:

  - Establecer o devolver el nombre de un parámetro con la propiedad [Name](name-property-ado.md).

  - Establecer o devolver el valor de un parámetro con la propiedad [Value](value-property-ado.md). **Value** es la propiedad predeterminada del objeto **Parameter**.

  - Establecer o devolver las características de los parámetros con las propiedades [Attributes](attributes-property-ado.md), [Direction](direction-property-ado.md), [Precision](precision-property-ado.md), [NumericScale](numericscale-property-ado.md), [Size](size-property-ado.md) y [Type](type-property-ado.md).

  - Pasar datos de caracteres largos o binarios largos a un parámetro con el método [AppendChunk](appendchunk-method-ado.md).

  - Obtener acceso a atributos específicos del proveedor con la colección [Properties](properties-collection-ado.md).

Si sabe los nombres y las propiedades de los parámetros asociados al procedimiento almacenado o a la consulta parametrizada que desea invocar, puede usar el método [CreateParameter](createparameter-method-ado.md) para crear objetos **Parameter** con los valores de propiedad adecuados, y utilizar el método [Append](append-method-ado.md) para agregarlos a la colección [Parameters](parameters-collection-ado.md). Esto permite establecer y devolver valores de parámetro sin tener que llamar al método [Refresh](refresh-method-ado.md) en la colección **Parameters** para recuperar la información sobre parámetros del proveedor, una operación que puede utilizar muchos recursos.

