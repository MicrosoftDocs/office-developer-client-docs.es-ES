---
title: Propiedad DBEngine.Version (DAO)
TOCTitle: Version Property
ms:assetid: b2807dc1-604f-4423-289a-ff38a3d9f31b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822024(v=office.15)
ms:contentKeyID: 48547171
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052986
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7e22645127f18ad815c398fd38f9ac4615dfadc9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294193"
---
# <a name="dbengineversion-property-dao"></a>Propiedad DBEngine.Version (DAO)


**Se aplica a:** Access 2013, Office 2013

Devuelve la versión de DAO que se está utilizando. **String** de sólo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . Versión

*expression* Variable que representa un objeto **DBEngine**.

## <a name="remarks"></a>Comentarios

El valor devuelto es un tipo de datos String que se evalúa en un número de versión en el formato "major.minor". Por ejemplo, "3.0". El número de versión del producto consta del número de versión (3), un punto y el número de lanzamiento (0).

