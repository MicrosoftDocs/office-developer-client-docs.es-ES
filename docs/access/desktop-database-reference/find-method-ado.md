---
title: Busque el método - ActiveX Data Objects (ADO)
TOCTitle: Find Method (ADO)
ms:assetid: a7cc9ceb-fdb9-73e2-8328-70b174f93cda
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249776(v=office.15)
ms:contentKeyID: 48546887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fc78503008daa733e747923697f21917ada8c106
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484636"
---
# <a name="find-method-ado"></a>Find (método, ADO)


**Se aplica a**: Access 2013 | Office 2013


Busca en un objeto [Recordset](recordset-object-ado.md) la fila que cumpla los criterios especificados. De manera opcional, se puede especificar la dirección de la búsqueda, la fila inicial y el desplazamiento desde la fila inicial. Si se cumplen los criterios, la posición de fila actual se establece en el registro encontrado; en caso contrario, se establece en el final (o el inicio) del objeto **Recordset**.

## <a name="syntax"></a>Sintaxis

Buscar (*criterios*, *SkipRows*, *SearchDirection*, *Iniciar*)

## <a name="parameters"></a>Parámetros

  - *Criteria*

  - Valor de tipo **String** con una instrucción que especifica el nombre de columna, el operador de comparación y el valor que se van a utilizar en la búsqueda.

  - *SkipRows*

  - Es opcional *.* Valor de tipo **Long**, cuyo valor predeterminado es cero, que especifica el desplazamiento con respecto a la fila actual o el marcador *Start* para iniciar la búsqueda. De forma predeterminada, la búsqueda inicia en la fila actual.

  - *SearchDirection*

  - Es opcional *.* Valor de [SearchDirectionEnum](searchdirectionenum.md) que especifica si la búsqueda debe iniciar en la fila actual o la siguiente fila disponible en dirección de la búsqueda. Una búsqueda sin resultados se detiene al final del objeto **Recordset** si el valor es **adSearchForward**. Una búsqueda sin resultados se detiene al principio del objeto **Recordset** si el valor es **adSearchBackward**.

  - *Start*

  - Es opcional. Marcador de tipo **Variant** que funciona como posición inicial de la búsqueda.

## <a name="remarks"></a>Comentarios

Se puede especificar únicamente el nombre de una sola columna en *Criteria*. Este método no admite búsquedas en varias columnas.

Es posible que el operador de comparación en *Criteria* "**\>**"(mayor que),"**\<**"(menor que), "=" (igual a),"\>=" (mayor o igual que), "\<=" (menor o igual que), "\<\>" (no igual a), o "like" (coincidencia de modelos).

El valor especificado en *Criteria* puede ser una cadena, un número de punto flotante o una fecha. Valores de cadena se delimitan con comillas simples o "\#" (signo de número) marca (por ejemplo, "estado = 'WA'" o "estado = \#WA\#"). Los valores de fecha se delimitan con "\#" (signo de número) marca (por ejemplo, "iniciar\_fecha \> \#22/7/97\#") y pueden contener horas, minutos y segundos para indicar las marcas de tiempo pero no deben contener milisegundos o se producirán errores .

Si el operador de comparación es "like", el valor de cadena puede contener un asterisco (\*) para que se busque una o varias apariciones de cualquier carácter o subcadena. Por ejemplo, "state like 'M\*'" encuentra Maine y Massachusetts. También se pueden utilizar asteriscos inicial y final para buscar una subcadena incluida en los valores. Por ejemplo, "state like '\*as\*' encuentra Alaska, Arkansas y Massachusetts.

Se pueden utilizar asteriscos sólo al final de la cadena, o bien, tanto al principio como al final de la cadena, tal y como se ha mostrado anteriormente. No se puede utilizar el asterisco como comodín inicial ('\*str') o comodín incrustado ('s\*r'). En caso contrario, se provocará un error.


> [!NOTE]
> <P>[!NOTA] Se producirá un error si no se establece una posición de fila actual antes de llamar a <STRONG>Find</STRONG>. Es preciso llamar a algún método que establezca la posición de fila, como el método <A href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</A>, antes de llamar a <STRONG>Find</STRONG>.</P>




> [!NOTE]
> <P>[!NOTA] Si llama al método <STRONG>Find</STRONG> en un conjunto de registros y la posición actual en el conjunto de registros se encuentra en el último registro o al final del archivo (EOF), la búsqueda no tendrá resultados. Deberá llamar al método <STRONG>MoveFirst</STRONG> para establecer el cursor o la posición actual en el inicio del conjunto de registros.</P>


