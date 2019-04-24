---
title: Propiedad QueryDef. LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 3b7818d4-054e-54e2-bf63-58b340bb4a90
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192665(v=office.15)
ms:contentKeyID: 48544287
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1876e92381828075edca3bbfcbae63e706a21365
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303314"
---
# <a name="querydeflastupdated-property-dao"></a>Propiedad QueryDef. LastUpdated (DAO)


**Se aplica a:** Access 2013, Office 2013

Devuelve la fecha y la hora del último cambio realizado en un objeto. **Variant** de sólo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . LastUpdated

*expresión* Variable que representa un objeto **QueryDef** .

## <a name="remarks"></a>Comentarios

**DateCreated** y **LastUpdated** devuelven la fecha y la hora en la que un objeto se creó o se actualizó por última vez. En un entorno multiusuario, los usuarios deben obtener estos valores directamente desde el servidor de archivos para evitar discrepancias con los valores de las propiedades DateCreated y LastUpdated.

