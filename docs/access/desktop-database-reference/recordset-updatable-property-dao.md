---
title: Propiedad Recordset.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 2d4bdcef-1b10-b542-ce0f-6172c271131b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192110(v=office.15)
ms:contentKeyID: 48543968
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a7f5d803c64504c598a96c244db3fcf75bf0dd5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919265"
---
# <a name="recordsetupdatable-property-dao"></a>Propiedad Recordset.Updatable (DAO)


**Se aplica a**: Access 2013, Office 2013

Devuelve un valor que indica si el usuario puede cambiar un objeto DAO. **Boolean** de sólo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . Actualizable

*expresión* Variable que representa un objeto **Recordset** .

## <a name="remarks"></a>Comentarios

Objetos Recordset de tipo Snapshot y forward-only siempre devuelven **False**.

Muchos tipos de objetos pueden contener campos que no se pueden actualizar. Por ejemplo, puede crear un objeto **Recordset** de tipo Dynaset en el que sólo se pueden modificar algunos campos. Estos campos pueden ser fijos o contener datos que se incrementen automáticamente, o el Dynaset puede resultar de una consulta que combina tablas actualizables y no actualizables.

Si el objeto únicamente contiene campos de sólo lectura, el valor de la propiedad **Updatable** es **False**. Si uno o más campos son actualizables, el valor de la propiedad es **True**. Sólo se pueden editar los campos actualizables. Si intenta asignar un nuevo valor a un campo de sólo lectura, se producirá un error capturable.

Como un objeto actualizable puede contener campos de solo lectura, compruebe la propiedad **DataUpdatable** de cada campo en la colección **Fields** de un objeto **Recordset** antes de modificar un registro.

