---
title: Propiedad Document.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 9307ceee-095f-0364-fd5b-905bc523b9c0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197661(v=office.15)
ms:contentKeyID: 48546388
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: abb766f7a47cbacaededf65eb2b5e9145bf88c60
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698382"
---
# <a name="documentlastupdated-property-dao"></a>Propiedad Document.LastUpdated (DAO)


**Se aplica a**: Access 2013, Office 2013

Devuelve la fecha y la hora del último cambio efectuado en un objeto. **Variant** de sólo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . LastUpdated

*expresión* Variable que representa un objeto **Document** .

## <a name="remarks"></a>Observaciones

**DateCreated** y **LastUpdated** devuelven la fecha y la hora en que se creó o actualizó por última vez el objeto. En un entorno multiusuario, los usuarios deben obtener estos valores directamente del servidor de archivos para evitar discrepancias en los valores de las propiedades DateCreated y LastUpdated.

