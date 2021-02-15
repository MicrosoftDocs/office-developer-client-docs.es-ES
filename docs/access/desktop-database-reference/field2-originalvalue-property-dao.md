---
title: Propiedad Field2.OriginalValue (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 10fed55e-c938-2ae6-8fd2-996745a63da3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845353(v=office.15)
ms:contentKeyID: 48543306
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101183
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3e3da5f7438ae83010c6ecc109dccf5d7a8eb9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292744"
---
# <a name="field2originalvalue-property-dao"></a>Propiedad Field2.OriginalValue (DAO)


**Se aplica a:** Access 2013, Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . OriginalValue

*expression* Variable que representa un objeto **Field2**.

## <a name="remarks"></a>Comentarios

Durante una actualización por lotes optimista, puede producirse un conflicto si el segundo cliente modifica el mismo campo y se registra en el intervalo de tiempo que transcurre desde que el primer cliente recupera los datos hasta que realiza un intento de actualización. La propiedad **OriginalValue** contiene el valor del campo al tiempo que comienza la última actualización por lotes **Update**. Si este valor no coincide con el valor real en la base de datos cuando la actualización por lotes **Update** intenta escribir en la base de datos, se produce un conflicto. Si esto ocurre, se tendrá acceso al nuevo valor en la base de datos a través de la propiedad **VisibleValue**.

