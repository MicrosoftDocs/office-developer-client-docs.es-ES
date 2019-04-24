---
title: Propiedad TableDef. DateCreated (DAO)
TOCTitle: DateCreated Property
ms:assetid: fedd28e9-41a4-db7f-9ba9-6ada350d594a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837292(v=office.15)
ms:contentKeyID: 48548947
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a5dc326b271e8444211bba0cd2d3c37c047ac205
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314542"
---
# <a name="tabledefdatecreated-property-dao"></a>Propiedad TableDef. DateCreated (DAO)


**Se aplica a:** Access 2013, Office 2013

Devuelve la fecha y la hora en la que se creó un objeto (sólo para áreas de trabajo de Microsoft Access). **Variant** de sólo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . CreateDate

*expresión* Variable que representa un objeto **TableDef** .

## <a name="remarks"></a>Comentarios

**DateCreated** y **LastUpdated** devuelven la fecha y la hora en la que un objeto se creó o se actualizó por última vez. En un entorno multiusuario, los usuarios deben obtener estos valores directamente desde el servidor de archivos para evitar discrepancias con los valores de las propiedades DateCreated y LastUpdated.

