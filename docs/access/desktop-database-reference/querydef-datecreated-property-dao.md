---
title: Propiedad QueryDef.DateCreated (DAO)
TOCTitle: DateCreated Property
ms:assetid: f7585b34-8314-fb9f-daa6-cd1a8ad59d91
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836910(v=office.15)
ms:contentKeyID: 48548763
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4a120eed6c20db73e1c23f31ea9329d00da2f0d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699684"
---
# <a name="querydefdatecreated-property-dao"></a>Propiedad QueryDef.DateCreated (DAO)


**Se aplica a**: Access 2013, Office 2013

Devuelve la fecha y la hora en que se creó un objeto (únicamente áreas de trabajo de Microsoft). **Variant** de sólo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . DateCreated

*expresión* Variable que representa un objeto **QueryDef** .

## <a name="remarks"></a>Observaciones

**DateCreated** y **LastUpdated** devuelven la fecha y la hora en que se creó o actualizó por última vez el objeto. En un entorno multiusuario, los usuarios deben obtener estos valores directamente del servidor de archivos para evitar discrepancias en los valores de las propiedades DateCreated y LastUpdated.

