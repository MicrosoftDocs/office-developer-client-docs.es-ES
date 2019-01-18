---
title: Documents.Refresh (método) (DAO)
TOCTitle: Refresh Method
ms:assetid: 33405192-f23c-e2a2-feb6-9d641439cbc5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192321(v=office.15)
ms:contentKeyID: 48544100
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b1e0ecf94a2442d742475bdf00311bbfa1e222f2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719186"
---
# <a name="documentsrefresh-method-dao"></a>Documents.Refresh (método) (DAO)


**Se aplica a**: Access 2013, Office 2013

Actualiza los objetos en la colección especificada para que reflejen el esquema actual de la base de datos.

## <a name="syntax"></a>Sintaxis

*expresión* . Actualización

*expresión* Variable que representa un objeto **Documents** .

## <a name="remarks"></a>Observaciones

El método **Refresh** se utiliza en entornos multiusuario en los que otros usuarios pueden cambiar la base de datos. Es posible que se deba utilizar también en cualquier colección que se vea afectada indirectamente por los cambios en la base de datos. Por ejemplo, si cambia una colección **Users**, es posible que necesite actualizar una colección **Groups** antes de utilizar esta colección **Groups**.

Una colección se rellena con objetos la primera vez que se hace referencia a ella y no reflejará automáticamente los cambios siguientes que realicen otros usuarios. Si es probable que otro usuario modifique una colección, utilice el método Refresh en la colección justo antes de ejecutar cualquier otra tarea en la aplicación que suponga la presencia o ausencia de un objeto en particular de la colección. Esto asegura que la colección esté lo más actualizada posible. Por otra parte, el uso de Refresh puede ralentizar innecesariamente el rendimiento.

