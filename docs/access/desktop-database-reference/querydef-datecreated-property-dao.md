---
title: Propiedad QueryDef. DateCreated (DAO)
TOCTitle: DateCreated Property
ms:assetid: f7585b34-8314-fb9f-daa6-cd1a8ad59d91
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836910(v=office.15)
ms:contentKeyID: 48548763
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4a120eed6c20db73e1c23f31ea9329d00da2f0d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301074"
---
# <a name="querydefdatecreated-property-dao"></a>Propiedad QueryDef. DateCreated (DAO)


**Se aplica a:** Access 2013, Office 2013

Devuelve la fecha y la hora en la que se creó un objeto (sólo para áreas de trabajo de Microsoft Access). **Variant** de sólo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . CreateDate

*expresión* Variable que representa un objeto **QueryDef** .

## <a name="remarks"></a>Comentarios

**DateCreated** y **LastUpdated** devuelven la fecha y la hora en la que un objeto se creó o se actualizó por última vez. En un entorno multiusuario, los usuarios deben obtener estos valores directamente desde el servidor de archivos para evitar discrepancias con los valores de las propiedades DateCreated y LastUpdated.

