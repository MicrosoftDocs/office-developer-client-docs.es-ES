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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293808"
---
# <a name="documentlastupdated-property-dao"></a>Propiedad Document.LastUpdated (DAO)


**Se aplica a:** Access 2013, Office 2013

Devuelve la fecha y la hora del último cambio realizado en un objeto. **Variant** de sólo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . LastUpdated

*expresión* Variable que representa un objeto **Document.**

## <a name="remarks"></a>Comentarios

**DateCreated** y **LastUpdated** devuelven la fecha y la hora en la que un objeto se creó o se actualizó por última vez. En un entorno multiusuario, los usuarios deben obtener estos valores directamente desde el servidor de archivos para evitar discrepancias con los valores de las propiedades DateCreated y LastUpdated.

