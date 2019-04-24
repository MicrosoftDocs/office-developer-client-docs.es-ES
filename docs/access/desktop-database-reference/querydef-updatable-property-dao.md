---
title: Propiedad QueryDef. Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5321e834f1dd5ed663033cacb530962d7beeb5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303335"
---
# <a name="querydefupdatable-property-dao"></a>Propiedad QueryDef. Updatable (DAO)


**Se aplica a:** Access 2013, Office 2013

Devuelve un valor que indica si el usuario puede cambiar un objeto DAO. **Boolean** de sólo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . Actualizable

*expresión* Variable que representa un objeto **QueryDef** .

## <a name="remarks"></a>Comentarios

La propiedad **Updatable** de un objeto **QueryDef** está establecida en **True** si se puede actualizar la consulta de definición, incluso si el objeto **[Recordset](recordset-object-dao.md)** resultante no es actualizable.

