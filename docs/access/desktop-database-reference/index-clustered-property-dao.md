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
ms.openlocfilehash: 4e7bd39d3329c83ec2a26fbef11e3a3b4e51e760
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921309"
---
# <a name="indexclustered-property-dao"></a>Propiedad Index.Clustered (DAO)


**Se aplica a**: Access 2013, Office 2013

Establece o devuelve un valor que indica si un objeto **Index** representa un índice agrupado para una tabla (sólo áreas de trabajo de Microsoft Access). **Boolean** de lectura y escritura.

## <a name="syntax"></a>Sintaxis

*expresión* . Agrupado

*expresión* Expresión que devuelve un objeto **Index** .

## <a name="remarks"></a>Observaciones

La configuración o el valor devuelto es un tipo de datos Boolean que es **True** si el objeto **Index** representa un índice agrupado.

Determinados formatos de base de datos de escritorio IISAM utilizan índices agrupados. Un índice agrupado consta de uno o varios campos que no son de clave, los cuales conjuntamente organizan todos los registros de una tabla en un orden predefinido. Un índice agrupado proporciona acceso eficaz a los registros de una tabla en la que los valores de índice pueden no ser únicos.

La propiedad **Clustered** es de lectura y escritura para un objeto **Index** nuevo que todavía no se ha anexado a una colección y de sólo lectura para un objeto **Index** existente de una colección **Indexes**.


> [!NOTE]
> <UL>
> <LI>
> <P>Las bases de datos del motor de base de datos de Microsoft Access omiten la propiedad <STRONG>Clustered</STRONG>, ya que el motor de base de datos de Microsoft Access no admite índices agrupados.</P>
> <LI>
> <P>Para los orígenes de datos ODBC, la propiedad <STRONG>Clustered</STRONG> siempre devuelve <STRONG>False</STRONG>; no detecta si el origen de datos ODBC tiene o no un índice agrupado.</P></LI></UL>


