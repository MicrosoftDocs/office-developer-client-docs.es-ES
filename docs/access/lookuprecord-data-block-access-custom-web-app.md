---
title: Bloque de datos BuscarRegistro (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: Un bloque de datos BuscarRegistro realiza un conjunto de acciones en un registro específico.
ms.openlocfilehash: 7012fecdf0e73647b2b8177473dd8b5540b5fcca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815368"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a>Bloque de datos BuscarRegistro (aplicación web personalizado de Access)

Un bloque de datos **BuscarRegistro** realiza un conjunto de acciones en un registro específico. 
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
> [!NOTE]
> [!NOTA] El bloque de datos **BuscarRegistro** solo está disponible en macros de datos. 
  
## <a name="setting"></a>Valores

La acción **EstablecerCampo** utiliza los siguientes argumentos. 
  
|**Argumento**|**Necesario**|**Descripción**|
|:-----|:-----|:-----|
| _En _ <br/> |Sí  <br/> |Una cadena que identifica el registro para funcionar en. El argumento *en* puede contener el nombre de la tabla, una consulta de selección o una instrucción SQL.  <br/> |
| _Where Condition_ <br/> |No  <br/> |Expresión de cadena utilizada para restringir el intervalo de datos en la que el bloque de datos **BuscarRegistro** se lleva a cabo. Por ejemplo, criterios con frecuencia es equivalente a la cláusula WHERE en una expresión SQL, sin la palabra donde. Si se omite criterios, el bloque de datos **BuscarRegistro** funciona en todo el dominio especificado por el argumento *en* . Cualquier campo que se incluya en criterios debe ser también un campo de *en* .  <br/> |
| _Alias_ <br/> |No  <br/> |Una cadena que proporciona un nombre alternativo para el registro especificado por el argumento *en* . A menudo se usa para acortar el nombre de tabla para las referencias subsiguientes a fin de evitar posibles referencias ambiguas. Si no se especifica el *Alias* , se usará el nombre de la tabla o consulta como el alias.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si los criterios especificados por los argumentos  *En*  y  *Condición WHERE*  especifican más de un registro, el bloque de datos **BuscarRegistro** solo operará en el primer registro. 
  
Si ningún registro cumple la *Condición Where* o si *en* no contiene ningún registro, **BuscarRegistro** crea un registro en blanco en el que todos los campos contienen un valor **nulo** . 
  

