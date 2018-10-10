---
title: Delete (método, Colección Parameters de ADO)
TOCTitle: Delete Method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 43d193a78be10ec5cedc2fe1a4001e677878dfb6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485569"
---
# <a name="delete-method-ado-parameters-collection"></a>Delete (método, Colección Parameters de ADO)


**Se aplica a**: Access 2013 | Office 2013


Elimina un objeto de la colección [Parameters](parameters-collection-ado.md).

## <a name="syntax"></a>Sintaxis

*Los parámetros*. Eliminar *índice*

## <a name="parameters"></a>Parámetros

  - *Index*

  - Valor de tipo **String** que contiene el nombre del objeto que se va a eliminar, o bien, la posición ordinal (índice) del objeto en la colección.

## <a name="remarks"></a>Comentarios

El uso del método **Delete** en una colección permite quitar uno de los objetos de la colección. Este método está disponible solo en la colección **Parameters** de un objeto [Command](command-object-ado.md). Debe usar la propiedad [Name](parameter-object-ado.md) del objeto [Parameter](name-property-ado.md) o su índice de colección al llamar al método **Delete**; una variable de objeto no es un argumento válido.

