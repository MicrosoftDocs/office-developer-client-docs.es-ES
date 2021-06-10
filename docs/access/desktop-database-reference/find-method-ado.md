---
title: 'Método Find: ActiveX Data Objects (ADO)'
TOCTitle: Find method (ADO)
ms:assetid: a7cc9ceb-fdb9-73e2-8328-70b174f93cda
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249776(v=office.15)
ms:contentKeyID: 48546887
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 32f14e4aeed669e68d976559932306c3cb76c696
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292415"
---
# <a name="find-method-ado"></a>Método Find (ADO)

**Se aplica a:** Access 2013, Office 2013

Busca en un objeto [Recordset](recordset-object-ado.md) la fila que cumpla los criterios especificados. De manera opcional, se puede especificar la dirección de la búsqueda, la fila inicial y el desplazamiento desde la fila inicial. Si se cumplen los criterios, la posición de fila actual se establece en el registro encontrado; en caso contrario, se establece en el final (o el inicio) del objeto **Recordset**.

## <a name="syntax"></a>Sintaxis

Buscar (*Criteria*, *SkipRows*, *SearchDirection*, *Start*)

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*Criterios* |Valor de tipo **String** con una instrucción que especifica el nombre de columna, el operador de comparación y el valor que se van a utilizar en la búsqueda.|
|*SkipRows* |Opcional. Valor de tipo **Long**, cuyo valor predeterminado es cero, que especifica el desplazamiento con respecto a la fila actual o el marcador *Start* para iniciar la búsqueda. De forma predeterminada, la búsqueda inicia en la fila actual.|
|*SearchDirection* |Opcional. Valor de [SearchDirectionEnum](searchdirectionenum.md) que especifica si la búsqueda debe iniciar en la fila actual o la siguiente fila disponible en dirección de la búsqueda. Una búsqueda sin resultados se detiene al final del objeto **Recordset** si el valor es **adSearchForward**. Una búsqueda sin resultados se detiene al principio del objeto **Recordset** si el valor es **adSearchBackward**.|
|*Start* |Es opcional. Marcador de tipo **Variant** que funciona como posición inicial de la búsqueda.|

## <a name="remarks"></a>Comentarios

Se puede especificar únicamente el nombre de una sola columna en *Criteria*. Este método no admite búsquedas en varias columnas.

El operador de comparación de *Criteria* puede ser " **\>** " (mayor que), **\<** " (menor que), "=" (igual), " \> =" (mayor o igual), " \< =" (menor o igual), " \< \> " (no igual) o "like" (coincidencia de patrones).

El valor especificado en *Criteria* puede ser una cadena, un número de punto flotante o una fecha. Los valores de cadena se delimitan con comillas simples o marcas " " (signo de \# número) (por ejemplo, "state = 'WA'" o "state = \# \# WA"). Los valores de fecha se delimitan con marcas " " (signo de \# número) (por ejemplo, "fecha de inicio \_ \> \# 7/22/97 ") y pueden contener horas, minutos y segundos para indicar marcas de tiempo, pero no deben contener milisegundos ni se producirán \# errores.

Si el operador de comparación es "like", el valor de cadena puede contener un asterisco (\*) para que se busque una o varias apariciones de cualquier carácter o subcadena. Por ejemplo, "state like 'M\*'" encuentra Maine y Massachusetts. También se pueden utilizar asteriscos inicial y final para buscar una subcadena incluida en los valores. Por ejemplo, "state like '\*as\*' encuentra Alaska, Arkansas y Massachusetts.

Se pueden utilizar asteriscos sólo al final de la cadena, o bien, tanto al principio como al final de la cadena, tal y como se ha mostrado anteriormente. No se puede utilizar el asterisco como comodín inicial ('\*str') o comodín incrustado ('s\*r'). En caso contrario, se provocará un error.

> [!NOTE]
> [!NOTA] Se producirá un error si no se establece una posición de fila actual antes de llamar a **Find**. Es preciso llamar a algún método que establezca la posición de fila, como el método [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), antes de llamar a **Find**.

> [!NOTE]
> [!NOTA] Si llama al método **Find** en un conjunto de registros y la posición actual en el conjunto de registros se encuentra en el último registro o al final del archivo (EOF), la búsqueda no tendrá resultados. Deberá llamar al método **MoveFirst** para establecer el cursor o la posición actual en el inicio del conjunto de registros.


