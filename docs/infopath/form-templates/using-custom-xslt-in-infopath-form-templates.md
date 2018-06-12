---
title: Usar XSLT personalizado en plantillas de formulario de InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 32c80bcd-a5d6-af32-38ba-9ca9ff148b99
description: Puede crear la mayoría de los elementos de la vista que probablemente necesite en el diseñador de formularios Microsoft InfoPath. Si necesita un elemento de vista personalizada que InfoPath no puede crear, podrá modificar manualmente la transformación XSL (XSLT) que InfoPath usa para generar la vista. Para hacerlo, extraiga el formulario dentro de los archivos de componente mediante Exportar archivos de origen en la pestaña Publicar de Microsoft Office Backstage y, a continuación, edite la transformación en su editor XML preferido, como Microsoft Visual Studio o Bloc de notas.
ms.openlocfilehash: 796115c99c81fc2a77812d91d317f5ce9ed54e5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815978"
---
# <a name="using-custom-xslt-in-infopath-form-templates"></a><span data-ttu-id="421d9-105">Usar XSLT personalizado en plantillas de formulario de InfoPath</span><span class="sxs-lookup"><span data-stu-id="421d9-105">Using Custom XSLT in InfoPath Form Templates</span></span>

<span data-ttu-id="421d9-p102">Puede crear la mayoría de los elementos de la vista que probablemente necesite en el diseñador de formularios Microsoft InfoPath. Si necesita un elemento de vista personalizada que InfoPath no puede crear, podrá modificar manualmente la transformación XSL (XSLT) que InfoPath usa para generar la vista. Para hacerlo, extraiga el formulario dentro de los archivos de componente mediante **Exportar archivos de origen** en la pestaña **Publicar** de Microsoft Office Backstage y, a continuación, edite la transformación en su editor XML preferido, como Microsoft Visual Studio o Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="421d9-p102">You can create most of the view elements you're likely to need in the Microsoft InfoPath form designer. If you need a custom view element that InfoPath can't create for you, however, you can manually modify the XSL Transformation (XSLT) that InfoPath uses to generate the view. To do so, extract the form into its component files by using **Export Source Files** on the **Publish** tab of the Microsoft Office Backstage, and then edit the transform in your preferred XML editor, such as Microsoft Visual Studio or Notepad.</span></span> 
  
<span data-ttu-id="421d9-p103">Si realiza cambios en una transformación de vista fuera de InfoPath y, a continuación, abre la vista en modo de diseño y realiza cambios, InfoPath sobrescribirá los cambios que realizó manualmente. Para evitar que InfoPath sobrescriba los cambios realizados, debe colocar esos cambios en un elemento  `<xsl:template>` de la transformación y usar el modo  `xd:preserve`, como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="421d9-p103">If you make changes to a view transform outside of InfoPath and then open the view in design mode and make changes, InfoPath will overwrite the changes you made manually. To keep InfoPath from overwriting the changes you make, you must place those changes in an  `<xsl:template>` element in the transform and use the  `xd:preserve` mode, as shown here:</span></span> 
  
```XML
<xsl:template match="my:field1" mode="xd:preserve"> 
   <div> 
      The value of field1 is <xsl:value-of select="."/> 
   </div> 
</xsl:template>
```

<span data-ttu-id="421d9-111">Para incluir la plantilla en el archivo transformado, use el elemento  `<xsl:apply-templates>` con el mismo modo  `xd:preserve`:</span><span class="sxs-lookup"><span data-stu-id="421d9-111">To include the template in the transformed file, use the  `<xsl:apply-templates>` element with the same  `xd:preserve` mode:</span></span> 
  
```XML
<xsl:apply-templates select="my:field1" mode="xd:preserve"/>
```

<span data-ttu-id="421d9-p104">Los elementos y constructores definidos dentro de plantillas XSL con el modo  `xd:preserve` no se mostrarán en el entorno de diseño de InfoPath. InfoPath marcará la sección personalizada con un control con la etiqueta **Conservar bloque de código** con un borde rojo. Cuando un usuario abra el formulario para rellenarlo, se aplicarán las transformaciones XSL personalizadas y los controles **Conservar bloque de código** no aparecerán.</span><span class="sxs-lookup"><span data-stu-id="421d9-p104">Elements and constructs defined within XSL templates with the  `xd:preserve` mode will not be displayed in the InfoPath design environment. Instead, InfoPath will mark the custom section with a control labeled **Preserve Code Block** with a red border. When a user opens the form to fill it out, the custom XSL transforms are applied and the **Preserve Code Block** controls will not appear.</span></span> 
  

