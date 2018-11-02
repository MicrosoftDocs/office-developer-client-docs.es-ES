---
title: Propiedad Field.OriginalValue (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 69ccec1e-311f-6905-e7bb-ad7fa8277494
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195384(v=office.15)
ms:contentKeyID: 48545418
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d850ebcfef6ea2c08e20ed953dfcc7b5ea23cbab
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926797"
---
# <a name="fieldoriginalvalue-property-dao"></a>Propiedad Field.OriginalValue (DAO)


**Se aplica a**: Access 2013, Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . OriginalValue

*expresión* Variable que representa un objeto **Field** .

## <a name="remarks"></a>Observaciones

Durante una actualización por lotes optimista, puede producirse un conflicto si el segundo cliente modifica el mismo campo y se registra en el intervalo de tiempo que transcurre desde que el primer cliente recupera los datos hasta que realiza un intento de actualización. La propiedad **OriginalValue** contiene el valor del campo al tiempo que comienza la última actualización por lotes **Update**. Si este valor no coincide con el valor real en la base de datos cuando la actualización por lotes **Update** intenta escribir en la base de datos, se produce un conflicto. Si esto ocurre, se tendrá acceso al nuevo valor en la base de datos a través de la propiedad **[VisibleValue](field-visiblevalue-property-dao.md)**.

