---
title: Parameters (colección) (ADO)
TOCTitle: Parameters Collection (ADO)
ms:assetid: 554387c3-3572-5391-3b24-c7d3443844cd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249283(v=office.15)
ms:contentKeyID: 48544923
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231103
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 96d2f4094c6b0df43e1579d7d35cbb78c12cc39c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484560"
---
# <a name="parameters-collection-ado"></a>Parameters (colección) (ADO)


**Se aplica a**: Access 2013 | Office 2013

Contiene todos los objetos [Parameter](parameter-object-ado.md) de un objeto [Command](command-object-ado.md).

## <a name="remarks"></a>Comentarios

Los objetos **Command** tienen una colección **Parameters** formada por objetos **Parameter**.

Si se usa el método [Refresh](refresh-method-ado.md) en la colección **Parameters** de un objeto **Command**, se recupera la información de parámetros del proveedor para el procedimiento almacenado o la consulta parametrizada especificados en el objeto **Command**. Algunos proveedores no admiten llamadas a procedimientos almacenados ni consultas parametrizadas. La llamada al método **Refresh** en la colección **Parameters** cuando se usa un proveedor de este tipo devolverá un error.

Si no ha definido sus propios objetos **Parameter** y obtiene acceso a la colección **Parameters** antes de llamar al método **Refresh**, ADO realizará automáticamente la llamada al método y el relleno de la colección.

Puede reducir al mínimo las llamadas al proveedor para mejorar el rendimiento si sabe las propiedades de los parámetros asociados al procedimiento almacenado o a la consulta parametrizada que desea invocar. Utilice el método [CreateParameter](createparameter-method-ado.md) para crear objetos **Parameter** con los valores de propiedad adecuados y utilice el método [Append](append-method-ado.md) para agregarlos a la colección **Parameters**. Esto le permite establecer y devolver los valores de parámetro sin tener que llamar al proveedor para obtener la información de los parámetros. Si escribe a un proveedor que no proporciona información de parámetros, debe rellenar manualmente la colección **Parameters** utilizando este método para poder usar parámetros. Utilice el método [Delete](delete-method-ado-parameters-collection.md) para quitar objetos **Parameter** de la colección **Parameters** si es necesario.

Los objetos de la colección **Parameters** de un objeto **Recordset** quedan fuera del ámbito (y, por lo tanto, no están disponibles) cuando el objeto **Recordset** está cerrado.

