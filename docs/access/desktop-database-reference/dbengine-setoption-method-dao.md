---
title: Método DBEngine.SetOption (DAO)
TOCTitle: SetOption Method
ms:assetid: ea55c10c-2385-1b7e-0cba-32982c9b6643
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836236(v=office.15)
ms:contentKeyID: 48548461
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1088781
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 55baceac9523400c5e646fbc4c1e7bb411219697
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998591"
---
# <a name="dbenginesetoption-method-dao"></a>Método DBEngine.SetOption (DAO)

**Se aplica a**: Access 2013, Office 2013

Anula temporalmente los valores para las claves del motor de base de datos de Microsoft Access en el Registro de Windows (solo áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . SetOption (***opción***, ***valor***)

*expresión* Una expresión que devuelve un objeto **DBEngine** .

## <a name="parameters"></a>Parámetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Obligatorio/opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Opción</em></p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Constante tal como se describe en Comentarios.</p></td>
</tr>
<tr class="even">
<td><p><em>Value</em></p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>El valor que se desea establecer la opción.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Observaciones

Cada constante hace referencia a la clave del registro correspondiente en la ruta de acceso HKEY\_LOCAL\_máquina\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\motores\\ACE (es decir, **dbSharedAsyncDelay** corresponde a la clave HKEY\_LOCAL\_máquina\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\motores\\ACE \\SharedAsyncDelay, y así sucesivamente).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbPageTimeout</strong></p></td>
<td><p>Clave PageTimeout</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSharedAsyncDelay</strong></p></td>
<td><p>Clave SharedAsyncDelay</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbExclusiveAsyncDelay</strong></p></td>
<td><p>Clave ExclusiveAsyncDelay</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLockRetry</strong></p></td>
<td><p>Clave LockRetry</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbUserCommitSync</strong></p></td>
<td><p>Clave UserCommitSync</p></td>
</tr>
<tr class="even">
<td><p><strong>dbImplicitCommitSync</strong></p></td>
<td><p>Clave ImplicitCommitSync</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbMaxBufferSize</strong></p></td>
<td><p>Clave MaxBufferSize</p></td>
</tr>
<tr class="even">
<td><p><strong>dbMaxLocksPerFile</strong></p></td>
<td><p>Clave MaxLocksPerFile</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLockDelay</strong></p></td>
<td><p>Clave LockDelay</p></td>
</tr>
<tr class="even">
<td><p><strong>dbRecycleLVs</strong></p></td>
<td><p>Clave RecycleLVs</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFlushTransactionTimeout</strong></p></td>
<td><p>Clave FlushTransactionTimeout</p></td>
</tr>
</tbody>
</table>


Utilice el método **SetOption** para anular los valores de registro en tiempo de ejecución. Los nuevos valores establecidos con el método **SetOption** siguen en vigor hasta que se cambien de nuevo mediante otra llamada **SetOption** o que se cierre el objeto **DBEngine**.

