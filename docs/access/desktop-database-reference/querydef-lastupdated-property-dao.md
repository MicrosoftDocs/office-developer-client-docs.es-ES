---
title: QueryDef.LastUpdated Property (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 3b7818d4-054e-54e2-bf63-58b340bb4a90
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192665(v=office.15)
ms:contentKeyID: 48544287
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 37a95cefb5af5070470fb5973076e230d76c3d98
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486728"
---
# <a name="querydeflastupdated-property-dao"></a>QueryDef.LastUpdated Property (DAO)


**Se aplica a**: Access 2013 | Office 2013

Devuelve la fecha y la hora del último cambio efectuado en un objeto. **Variant** de sólo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . LastUpdated

*expresión* Variable que representa un objeto **QueryDef** .

## <a name="remarks"></a>Observaciones

**DateCreated** y **LastUpdated** devuelven la fecha y la hora en que se creó o actualizó por última vez el objeto. En un entorno multiusuario, los usuarios deben obtener estos valores directamente del servidor de archivos para evitar discrepancias en los valores de las propiedades DateCreated y LastUpdated.

