---
title: Bloque de datos ForEachRecord (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: Un bloque de datos ForEachRecord repite un conjunto de instrucciones para cada registro de un dominio.
ms.openlocfilehash: 9715824bff7d478fa2880ada5e8770f7a0c88883
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428238"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a>Bloque de datos ForEachRecord (aplicación web personalizada de Access)

Un **bloque de datos ForEachRecord** repite un conjunto de instrucciones para cada registro de un dominio. 
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
> [!NOTE]
> El bloque de datos **ParaCadaRegistro** solo está disponible en macros de datos. 
  
## <a name="setting"></a>Configuración

La acción **ParaCadaRegistro** utiliza los siguientes argumentos. 
  
|**Nombre de argumento**|**Obligatorio**|**Descripción**|
|:-----|:-----|:-----|
|**In** <br/> |Sí  <br/> |Una cadena que identifica el dominio de los registros en los que se operará. El *argumento In* puede contener el nombre de la tabla, una consulta select o una instrucción SQL.  <br/> **NOTA:** el dominio especificado no puede incluir datos almacenados en una tabla vinculada u origen de datos ODBC.           |
|**Where Condition** <br/> |No  <br/> |Expresión de cadena usada para restringir el intervalo de datos en el que se realiza el bloque de datos **ForEachRecord.** Por ejemplo, los criterios a menudo equivalen a la cláusula WHERE en una expresión SQL, sin la palabra WHERE. Si se omiten criterios, el bloque de datos **ForEachRecord** funciona en todo el dominio especificado por el *argumento In.* Cualquier campo que se incluya en criteria también debe ser un campo en  *In*  .  <br/> |
|**Alias** <br/> |No  <br/> |Cadena que proporciona un nombre alternativo para el dominio especificado por el *argumento In.* Se utiliza a menudo para acortar el nombre de la tabla en referencias posteriores con el fin de evitar posibles referencias ambiguas. Si no se especifica  *Alias,*  se usará el nombre de la tabla o consulta como alias.  <br/> |
   
## <a name="remarks"></a>Comentarios

Utilice la acción **[SalirDeCadaRegistro](exitforeachrecord-macro-action-access-custom-web-app.md)** para salir inmediatamente de un bloque de datos **ParaCadaRegistro**. 
  

