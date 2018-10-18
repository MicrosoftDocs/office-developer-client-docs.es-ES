---
<<<<<<< Título HEAD: personalizado propiedades de cuadro de diálogo cuadro TOCTitle del ActiveX Control: ms:assetid del cuadro de diálogo de propiedades personalizadas del ActiveX Control: 124cf679-6efc-567a-84d1-8057dec93bde ms:mtpsurl: https://msdn.microsoft.com/library/Ff845396(v=office.15) ms:contentKeyID: 48543338 MS.Date: 18/09/2015 === título: cuadro de diálogo de propiedades personalizadas de control ActiveX TOCTitle: descripción del cuadro de diálogo de ActiveX control propiedades personalizadas: este cuadro de diálogo de propiedades personalizadas ofrece una alternativa a la lista de propiedades en el Microsoft Access hoja de propiedades para establecer las propiedades de control de ActiveX en la vista Diseño.
MS:AssetId: 124cf679-6efc-567a-84d1-8057dec93bde ms:mtpsurl: https://msdn.microsoft.com/library/Ff845396(v=office.15) ms:contentKeyID: ms.date 48543338: 16/10/2018
>>>>>>> maestro mtps_version: Office.15 f1_keywords:
- vbaac10.chm4040 f1_categories:
- Office.Version=v15
---

<<<<<<< HEAD
# <a name="activex-controls-custom-properties-dialog-box"></a>Cuadro de diálogo de propiedades personalizadas del Control ActiveX
=======
# <a name="activex-control-custom-properties-dialog-box"></a>Cuadro de diálogo de propiedades personalizadas de control de ActiveX
>>>>>>> master

**Se aplica a**: Access 2013 | Office 2013

Al establecer las propiedades de un control ActiveX, puede necesitar o preferir el uso del cuadro de diálogo de propiedades personalizadas del control. Este cuadro de diálogo de propiedades personalizadas ofrece una alternativa a la lista de propiedades de la hoja de propiedades de Microsoft Access para establecer las propiedades del control ActiveX en la vista Diseño.

> [!NOTE]
> [!NOTA] Esta información sólo tiene aplicación para controles ActiveX en el entorno de una base de datos de Microsoft Access.

<<<<<<< HEAD


## <a name="two-ways-to-set-properties"></a>Dos modos de establecer las propiedades
=======
## <a name="two-ways-to-set-properties"></a>Dos modos de establecer las propiedades
>>>>>>> master

La razón de ser del cuadro de diálogo de propiedades personalizadas es que no todas las aplicaciones que usan controles ActiveX ofrecen una hoja de propiedades como la de Microsoft Access. El cuadro de diálogo de propiedades personalizadas ofrece una interfaz para establecer las propiedades clave del control sea cual sea la interfaz suministrada por la aplicación.

Para algunas propiedades de los controles ActiveX, es posible elegir establecer las propiedades en:

<<<<<<< HEAD
  - La hoja de propiedades de Microsoft Access.

  - El cuadro de diálogo de propiedades personalizadas del control ActiveX.

En algunos casos, el cuadro de diálogo de propiedades personalizadas es el único medio disponible para establecer una propiedad en la vista Diseño. Ésta es normalmente la situación cuando la interfaz necesaria para establecer una propiedad no funciona dentro de la hoja de propiedades de Microsoft Access. Por ejemplo, la propiedad **FuenteDeCuadrícula (GridFont)** del control Calendar tiene varios argumentos; no es posible establecer más de un argumento para cada propiedad en la hoja de propiedades de Microsoft Access.

## <a name="finding-the-custom-properties-dialog-box"></a>Localizar el Cuadro de diálogo de propiedades personalizadas

No todos los controles ActiveX ofrecen un cuadro de diálogo de propiedades personalizadas. Para ver si un control ofrece este cuadro de diálogo de propiedades personalizadas, busque la propiedad **Personalizado (Custom)** en la hoja de propiedades de Microsoft Access para este control. Si la lista de propiedades incluye **Personalizado**, entonces el control dispone de cuadro de diálogo de propiedades personalizadas.

## <a name="using-the-custom-properties-dialog-box"></a>Utilización del Cuadro de diálogo de propiedades personalizadas

Después de hacer clic en el cuadro de la propiedad **Personalizado** en la hoja de propiedades de Microsoft Access, haga clic en el botón **Generar** situado a la derecha del cuadro de la propiedad para mostrar el cuadro de diálogo de propiedades personalizadas del control, a menudo presentada en forma de cuadro de diálogo con fichas. Seleccione la ficha que contenga la interfaz para las propiedades que desee establecer.

Después de realizar cambios en una ficha, normalmente se pueden aplicar dichos cambios inmediatamente haciendo clic en el botón **Aplicar** (si está presente). Puede hacer clic en otras pestañas para establecer otras propiedades según sus necesidades. Para confirmar todos los cambios en el cuadro de diálogo de propiedades personalizadas, haga clic en el botón **Aceptar**. Para volver a la hoja de propiedades de Microsoft Access sin cambiar los valores de ninguna propiedad, haga clic en el botón **Cancelar**.

También puede ver el cuadro de diálogo de propiedades personalizadas haciendo clic en el subcomando **Propiedades** del comando **Objeto** del control ActiveX (por ejemplo, **Objeto Control de calendario**) del menú **Edición**, o haciendo clic en este mismo subcomando en el menú contextual del control ActiveX. Además, algunas propiedades de la hoja de propiedades de Microsoft Access para el control ActiveX, como la propiedad **GridFontColor** del control Calendar, disponen de un botón **Generar** situado a la derecha del cuadro de la propiedad. Al hacer clic en el botón **Generar**, se muestra el cuadro de diálogo de propiedades personalizadas, con la ficha correspondiente ya seleccionada (por ejemplo, **Colores**).
=======
- La hoja de propiedades de Microsoft Access.
- El cuadro de diálogo de propiedades personalizadas del control ActiveX.

En algunos casos, el cuadro de diálogo de propiedades personalizadas es el único medio disponible para establecer una propiedad en la vista Diseño. Ésta es normalmente la situación cuando la interfaz necesaria para establecer una propiedad no funciona dentro de la hoja de propiedades de Microsoft Access. Por ejemplo, la propiedad **FuenteDeCuadrícula (GridFont)** del control Calendar tiene varios argumentos; no es posible establecer más de un argumento para cada propiedad en la hoja de propiedades de Microsoft Access.

## <a name="finding-the-custom-properties-dialog-box"></a>Localizar el cuadro de diálogo de propiedades personalizadas

No todos los controles ActiveX ofrecen un cuadro de diálogo de propiedades personalizadas. Para ver si un control ofrece este cuadro de diálogo de propiedades personalizadas, busque la propiedad **Personalizado (Custom)** en la hoja de propiedades de Microsoft Access para este control. Si la lista de propiedades contiene el nombre **personalizado**, el control dispone del cuadro de diálogo de propiedades personalizadas.

## <a name="using-the-custom-properties-dialog-box"></a>Mediante el cuadro de diálogo de propiedades personalizadas

Después de elegir el cuadro de la propiedad **personalizada** en la hoja de propiedades de Microsoft Access, elija el botón **Generar** a la derecha del cuadro de propiedad para mostrar el cuadro de diálogo de propiedades personalizadas del control, a menudo se muestra como un cuadro de diálogo con fichas. Seleccione la ficha que contenga la interfaz para las propiedades que desee establecer.

Después de realizar cambios en una ficha, normalmente se pueden aplicar estos cambios inmediatamente eligiendo el botón **Aplicar** (si se proporciona). Puede elegir otras fichas para establecer otras propiedades según sea necesario. Para aprobar todos los cambios realizados en el cuadro de diálogo de propiedades personalizadas, elija el botón **Aceptar** . Para volver a la hoja de propiedades de Microsoft Access sin cambiar los valores de propiedad, seleccione el botón **Cancelar** .

También puede ver el cuadro de diálogo de propiedades personalizadas, elija el subcomando **Propiedades** del comando **objeto** (por ejemplo, el **Objeto de Control Calendar**) del control de ActiveX en el menú **Edición** , o eligiendo este mismo subcomando en el menú contextual para el control ActiveX. Además, algunas propiedades de la hoja de propiedades de Microsoft Access para el control ActiveX, como la propiedad **ColorDeFuenteDeCuadrícula (GridFontColor)** del control Calendar, disponen de un botón **Generar** a la derecha del cuadro de la propiedad. Cuando elija el botón **Generar** , se muestra el cuadro de diálogo de propiedades personalizadas, con la ficha correspondiente ya seleccionada (por ejemplo, **colores**).
>>>>>>> master

