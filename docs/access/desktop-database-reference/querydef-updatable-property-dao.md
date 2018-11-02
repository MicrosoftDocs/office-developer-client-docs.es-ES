---
title: Propiedad QueryDef.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b0c1a85029270641a944d822ee81954ca1f2528e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919811"
---
# <a name="querydefupdatable-property-dao"></a>Propiedad QueryDef.Updatable (DAO)


**Se aplica a**: Access 2013, Office 2013

Devuelve un valor que indica si el usuario puede cambiar un objeto DAO. **Boolean** de sólo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . Actualizable

*expresión* Variable que representa un objeto **QueryDef** .

## <a name="remarks"></a>Observaciones

La propiedad **Updatable** de un objeto **QueryDef** está establecida en **True** si se puede actualizar la consulta de definición, incluso si el objeto **[Recordset](recordset-object-dao.md)** resultante no es actualizable.

