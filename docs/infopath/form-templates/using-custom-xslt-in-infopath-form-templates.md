---
title: Usar XSLT personalizado en plantillas de formulario de InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 32c80bcd-a5d6-af32-38ba-9ca9ff148b99
description: Puede crear la mayoría de los elementos de la vista que probablemente necesite en el diseñador de formularios Microsoft InfoPath. Si necesita un elemento de vista personalizada que InfoPath no puede crear, podrá modificar manualmente la transformación XSL (XSLT) que InfoPath usa para generar la vista. Para hacerlo, extraiga el formulario dentro de los archivos de componente mediante Exportar archivos de origen en la pestaña Publicar de Microsoft Office Backstage y, a continuación, edite la transformación en su editor XML preferido, como Microsoft Visual Studio o Bloc de notas.
ms.openlocfilehash: a61980191dbedeec33b06ad8173ce50126fea781
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428273"
---
# <a name="using-custom-xslt-in-infopath-form-templates"></a>Usar XSLT personalizado en plantillas de formulario de InfoPath

Puede crear la mayoría de los elementos de la vista que probablemente necesite en el diseñador de formularios Microsoft InfoPath. Si necesita un elemento de vista personalizada que InfoPath no puede crear, podrá modificar manualmente la transformación XSL (XSLT) que InfoPath usa para generar la vista. Para hacerlo, extraiga el formulario dentro de los archivos de componente mediante **Exportar archivos de origen** en la pestaña **Publicar** de Microsoft Office Backstage y, a continuación, edite la transformación en su editor XML preferido, como Microsoft Visual Studio o Bloc de notas. 
  
Si realiza cambios en una transformación de vista fuera de InfoPath y, a continuación, abre la vista en modo de diseño y realiza cambios, InfoPath sobrescribirá los cambios que realizó manualmente. Para evitar que InfoPath sobrescriba los cambios realizados, debe colocar esos cambios en un elemento  `<xsl:template>` de la transformación y usar el modo  `xd:preserve`, como se muestra aquí: 
  
```XML
<xsl:template match="my:field1" mode="xd:preserve"> 
   <div> 
      The value of field1 is <xsl:value-of select="."/> 
   </div> 
</xsl:template>
```

Para incluir la plantilla en el archivo transformado, use el elemento  `<xsl:apply-templates>` con el mismo modo  `xd:preserve`: 
  
```XML
<xsl:apply-templates select="my:field1" mode="xd:preserve"/>
```

Los elementos y constructores definidos dentro de plantillas XSL con el modo  `xd:preserve` no se mostrarán en el entorno de diseño de InfoPath. InfoPath marcará la sección personalizada con un control con la etiqueta **Conservar bloque de código** con un borde rojo. Cuando un usuario abra el formulario para rellenarlo, se aplicarán las transformaciones XSL personalizadas y los controles **Conservar bloque de código** no aparecerán. 
  

