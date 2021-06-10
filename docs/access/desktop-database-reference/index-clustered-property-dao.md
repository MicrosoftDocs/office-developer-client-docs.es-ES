---
title: Propiedad Index.Clustered (DAO)
TOCTitle: Clustered Property
ms:assetid: dd0876a9-b7fe-c8c8-e675-5ed758ce5bd3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835375(v=office.15)
ms:contentKeyID: 48548149
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052930
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 060963dc47c933fee903cd9b220adb45c7f63df6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291855"
---
# <a name="indexclustered-property-dao"></a>Propiedad Index.Clustered (DAO)

**Se aplica a:** Access 2013, Office 2013

Establece o devuelve un valor que indica si un objeto **Index** representa un índice agrupado para una tabla (sólo áreas de trabajo de Microsoft Access). **Boolean** de lectura y escritura.

## <a name="syntax"></a>Sintaxis

*expresión* . Agrupado

*expresión* Expresión que devuelve un **objeto Index.**

## <a name="remarks"></a>Comentarios

La configuración o el valor devuelto es un tipo de datos Boolean que es **True** si el objeto **Index** representa un índice agrupado.

Determinados formatos de base de datos de escritorio IISAM utilizan índices agrupados. Un índice agrupado consta de uno o varios campos que no son de clave, los cuales conjuntamente organizan todos los registros de una tabla en un orden predefinido. Un índice agrupado proporciona acceso eficaz a los registros de una tabla en la que los valores de índice pueden no ser únicos.

La propiedad **Clustered** es de lectura y escritura para un objeto **Index** nuevo que todavía no se ha anexado a una colección y de sólo lectura para un objeto **Index** existente de una colección **Indexes**.

> [!NOTE]
> - Las bases de datos del motor de base de datos de Microsoft Access omiten la propiedad **Clustered**, ya que el motor de base de datos de Microsoft Access no admite índices agrupados.
> - Para orígenes de datos ODBC, la **propiedad Clustered** siempre devuelve **False**; no detecta si el origen de datos ODBC tiene o no un índice agrupado.


