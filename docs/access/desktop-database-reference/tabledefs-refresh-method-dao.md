---
title: TableDefs.Refresh Method (DAO)
TOCTitle: Refresh Method
ms:assetid: f76c1a3f-1561-ce1f-a535-a5a2179ea739
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836915(v=office.15)
ms:contentKeyID: 48548765
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 722099cc6eb342f6ee2abaef2543731f7588689c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484688"
---
# <a name="tabledefsrefresh-method-dao"></a>TableDefs.Refresh Method (DAO)


**Se aplica a**: Access 2013 | Office 2013

Actualiza los objetos en la colección especificada para que reflejen el esquema actual de la base de datos.

## <a name="syntax"></a>Sintaxis

*expresión* . Actualización

*expresión* Variable que representa un objeto **TableDefs** .

## <a name="remarks"></a>Observaciones

Para determinar la posición que usa el motor de base de datos de Microsoft Access para objetos **Field** en la colección **Fields** de un objeto **QueryDef**, **Recordset** o **TableDef**, use la propiedad **OrdinalPosition** de cada objeto **Field**. Es posible que cambiando la propiedad **OrdinalPosition** de un objeto **Field** no se cambie el orden de los objetos **Field** de la colección hasta que se use el método **Refresh**.

El método **Refresh** se utiliza en entornos multiusuario en los que otros usuarios pueden cambiar la base de datos. Es posible que se deba utilizar también en cualquier colección que se vea afectada indirectamente por los cambios en la base de datos. Por ejemplo, si cambia una colección **Users**, es posible que necesite actualizar una colección **Groups** antes de utilizar esta colección **Groups**.

Una colección se rellena con objetos la primera vez que se hace referencia a ella y no reflejará automáticamente los cambios siguientes que realicen otros usuarios. Si es probable que otro usuario modifique una colección, utilice el método Refresh en la colección justo antes de ejecutar cualquier otra tarea en la aplicación que suponga la presencia o ausencia de un objeto en particular de la colección. Esto asegura que la colección esté lo más actualizada posible. Por otra parte, el uso de Refresh puede ralentizar innecesariamente el rendimiento.

