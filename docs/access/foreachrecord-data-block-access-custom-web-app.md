---
title: Bloque de datos ParaCadaRegistro (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: Un bloque de datos ParaCadaRegistro repite un conjunto de instrucciones para cada registro en un dominio.
ms.openlocfilehash: 9715824bff7d478fa2880ada5e8770f7a0c88883
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302460"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a>Bloque de datos ParaCadaRegistro (aplicación web personalizada de Access)

Un bloque de datos **ParaCadaRegistro** repite un conjunto de instrucciones para cada registro en un dominio. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
> [!NOTE]
> El bloque de datos **ParaCadaRegistro** solo está disponible en macros de datos. 
  
## <a name="setting"></a>Configuración

La acción **ParaCadaRegistro** utiliza los siguientes argumentos. 
  
|**Nombre de argumento**|**Obligatorio**|**Descripción**|
|:-----|:-----|:-----|
|**A** <br/> |Sí  <br/> |Una cadena que identifica el dominio de los registros en los que se operará. El argumento *in* puede contener el nombre de la tabla, una consulta de selección o una instrucción SQL.  <br/> **Nota**: el dominio especificado no puede incluir datos almacenados en una tabla vinculada u origen de datos ODBC.           |
|**Where Condition** <br/> |No  <br/> |Expresión de cadena que se usa para restringir el intervalo de datos en el que se ejecuta el bloque de datos **ParaCadaRegistro** . Por ejemplo, los criterios a menudo equivalen a la cláusula WHERE en una expresión SQL, sin la palabra WHERE. Si se omiten los criterios, el bloque de datos **ParaCadaRegistro** opera en todo el dominio especificado por el argumento *in* . Cualquier campo que se incluya en Criteria también debe ser un campo en *en* .  <br/> |
|**Alias** <br/> |No  <br/> |Una cadena que proporciona un nombre alternativo para el dominio especificado por el argumento *in* . Se utiliza a menudo para acortar el nombre de la tabla en referencias posteriores con el fin de evitar posibles referencias ambiguas. Si no se especifica ningún *alias* , se utilizará el nombre de la tabla o consulta como alias.  <br/> |
   
## <a name="remarks"></a>Comentarios

Utilice la acción **[SalirDeCadaRegistro](exitforeachrecord-macro-action-access-custom-web-app.md)** para salir inmediatamente de un bloque de datos **ParaCadaRegistro**. 
  

