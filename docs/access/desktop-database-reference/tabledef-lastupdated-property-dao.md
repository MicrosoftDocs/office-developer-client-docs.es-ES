---
title: Propiedad TableDef.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: fafe54e2-2cf0-5874-92b9-6e20a65e77ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837164(v=office.15)
ms:contentKeyID: 48548859
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 994543132fb5323566bd876da066419d0986bd91
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308417"
---
# <a name="tabledeflastupdated-property-dao"></a>Propiedad TableDef.LastUpdated (DAO)


**Se aplica a:** Access 2013, Office 2013

Devuelve la fecha y la hora del último cambio realizado en un objeto. **Variant** de sólo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . LastUpdated

*expression* Variable que representa un objeto **TableDef**.

## <a name="remarks"></a>Comentarios

**DateCreated** y **LastUpdated** devuelven la fecha y la hora en la que un objeto se creó o se actualizó por última vez. En un entorno multiusuario, los usuarios deben obtener estos valores directamente desde el servidor de archivos para evitar discrepancias con los valores de las propiedades DateCreated y LastUpdated.

