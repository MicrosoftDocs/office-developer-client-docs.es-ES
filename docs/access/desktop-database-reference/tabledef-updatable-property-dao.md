---
title: Propiedad TableDef.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6e6c7409b89058c6be55d9fb83eb85c7af9fb9c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725976"
---
# <a name="tabledefupdatable-property-dao"></a>Propiedad TableDef.Updatable (DAO)


**Se aplica a**: Access 2013, Office 2013

Devuelve un valor que indica si el usuario puede cambiar un objeto DAO. **Boolean** de sólo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . Actualizable

*expresión* Variable que representa un objeto **TableDef** .

## <a name="remarks"></a>Observaciones

El valor de la propiedad **Updatable** siempre es **True** para un nuevo objeto **TableDef** creado y **False** para un objeto **TableDef** vinculado. Un objeto **TableDef** nuevo sólo se puede anexar a una base de datos para la que el usuario actual tenga permiso de escritura.

