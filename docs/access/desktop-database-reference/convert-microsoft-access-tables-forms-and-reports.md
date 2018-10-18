---
<<<<<<< Título HEAD: convertir las tablas de Microsoft Access, formularios e informes de TOCTitle: ms:assetid de convertir las tablas de Microsoft Access, formularios e informes: cc170e62-a663-60e8-4446-07a7a874b747 ms:mtpsurl: https://msdn.microsoft.com/library/Ff834413(v=office.15) ms:contentKeyID: ms.date 48547731: 18/09/2015 === título: convertir Microsoft Access tablas, formularios e informes a TOCTitle: convertir Microsoft Access tablas, formularios e informes a Descripción: los cambios introducidos por Microsoft Access 2002 pueden afectar al comportamiento de la versión 1. x o 2.0.
MS:AssetId: cc170e62-a663-60e8-4446-07a7a874b747 ms:mtpsurl: https://msdn.microsoft.com/library/Ff834413(v=office.15) ms:contentKeyID: ms.date 48547731: 16/10/2018
>>>>>>> maestro mtps_version: Office.15 f1_keywords:
- vbaac10.chm5187104 f1_categories:
- Office.Version=v15
---

<<<<<<< HEAD
# <a name="convert-microsoft-access-tables-forms-and-reports"></a>Convertir tablas, formularios e informes de Microsoft Access
=======
# <a name="convert-microsoft-access-tables-forms-and-reports"></a>Convertir tablas, formularios e informes de Microsoft Access
>>>>>>> master

**Se aplica a**: Access 2013 | Office 2013

Se han realizado varios cambios en Microsoft Access 2002 que pueden afectar al comportamiento de las aplicaciones de la versión 1.*x* o 2.0. Las siguientes secciones ofrecen información acerca de esos cambios.

<<<<<<< HEAD
## <a name="indexes-and-relationships"></a>Índices y relaciones

Una tabla de Microsoft Access puede contener hasta 32 índices. Las tablas muy complejas que forman parte de muchas relaciones pueden exceder el límite del índice, con lo que no será capaz de convertir la base de datos que contenga estas tablas. El motor de base de datos de Microsoft Access crea índices en ambos lados de las relaciones entre tablas. Si la base de datos no se convierte, elimine algunas relaciones e intente convertir de nuevo la base de datos.

## <a name="the-limittolist-property-of-combo-boxes"></a>La propiedad LimitarALista (LimitToList) de los cuadros combinados

En Microsoft Access 2002 o posterior, cuadros combinados aceptan valores **nulos** cuando la propiedad **LimitToList** se establece en **True** (-1), si la lista contiene valores **nulos** o no. En la versión 2.0, un cuadro combinado que tuviera la propiedad **LimitToList** establecida en **True** no aceptaría un valor **Null** a menos que la lista contuviera un valor **Null**. Si se desea evitar que los usuarios indiquen un valor **Null** mediante un cuadro combinado, establezca la propiedad **Required** del campo de la tabla en **Yes**.

## <a name="menus-and-in-place-activation-of-ole-objects"></a>Activar menús y complementos de los objetos OLE

Con la idea de poner a su disposición funcionalidades adicionales mientras se activan en el sitio objetos OLE, es posible que algunos comandos de menú se hayan movido a un menú que no se reemplace al activar un servidor OLE.

Las macros de la aplicación convertida que utilicen una acción EjecutarElementoMenú para ejecutar un comando de menú de la versión 2.0 al activar un servidor OLE, no se verán afectadas por los cambios. Los comandos de la versión 2.0 han sido relacionados con sus equivalentes de versiones posteriores de Microsoft Access.

## <a name="referencing-a-control-on-a-read-only-form"></a>Hacer referencia a un control en un formulario de sólo lectura

En Microsoft Access 2002 o posterior, no es posible utilizar una expresión para hacer referencia al valor de un control en un formulario de sólo lectura que sea dependiente de un origen de registro en blanco. En las versiones anteriores, la expresión devolvería un valor **Null**. Antes de hacer referencia a un control en un formulario que sea de sólo lectura, debe asegurarse de que el origen del registro del formulario contiene registros.

## <a name="date-fields-and-data-entry"></a>Campos de fecha y entrada de datos

Si se indica **3/3** en un campo de tipo Fecha en una hoja de datos de un formulario o una tabla, el año actual se agrega automáticamente en Microsoft Access 2002 o posterior. Sin embargo, si se indica **3/3/** en el mismo campo, Microsoft Access devolverá un mensaje de error. Debe omitir el último delimitador de la fecha de forma que Microsoft Access pueda traducir la fecha al formato adecuado.

## <a name="buttons-created-with-the-command-button-wizard"></a>Botones creados con el Asistente para botones

Si utilizó el Asistente para botones de comando en las versiones 2.0 o 7.0 de Microsoft Access para generar código que llama a otra aplicación, debe eliminar el botón y volver a crearlo usando el Asistente para botones de comando en Microsoft Access 2002 o posterior.

## <a name="form-and-report-class-modules"></a>Módulos de clase en formularios e informes

En las versiones anteriores a Microsoft Access 2002, los objetos **Form** y **Report** tenían asociados módulos de clase incluso cuando no había código detrás del objeto. En Microsoft Access 2002 o posterior, puede establecer en **False** la propiedad **HasModule** del formulario o informe. Cuando la propiedad **HasModule** se establece en **False**, el formulario o informe ocupa menos espacio en disco y se carga más rápidamente porque ya no tiene asociado un módulo de clase.

## <a name="converted-version-20-report-has-different-margins"></a>Los informes convertidos de la versión 2.0 tienen márgenes distintos
=======
## <a name="indexes-and-relationships"></a>Los índices y relaciones

Una tabla de Microsoft Access puede contener hasta 32 índices. Las tablas muy complejas que forman parte de muchas relaciones pueden exceder el límite del índice, con lo que no será capaz de convertir la base de datos que contenga estas tablas. El motor de base de datos de Microsoft Access crea índices en ambos lados de las relaciones entre tablas. Si la base de datos no se convierte, elimine algunas relaciones e intente convertir de nuevo la base de datos.

## <a name="the-limittolist-property-of-combo-boxes"></a>La propiedad LimitarALista (LimitToList) de los cuadros combinados

En Microsoft Access 2002 o posterior, cuadros combinados aceptan valores **nulos** cuando la propiedad **LimitToList** se establece en **True** (-1), si la lista contiene valores **nulos** o no. En la versión 2.0, un cuadro combinado que tuviera la propiedad **LimitToList** establecida en **True** no aceptaría un valor **Null** a menos que la lista contuviera un valor **Null**. Si se desea evitar que los usuarios indiquen un valor **Null** mediante un cuadro combinado, establezca la propiedad **Required** del campo de la tabla en **Yes**.

## <a name="menus-and-in-place-activation-of-ole-objects"></a>Los menús y la activación en contexto de objetos OLE

Para realizar funciones adicionales disponibles en durante la activación de los objetos OLE en contexto, algunos comandos de menú es posible que se ha movido a un menú que no sea reemplazado cuando se activa un servidor OLE.

Las macros de la aplicación convertida que utilicen una acción EjecutarElementoMenú para ejecutar un comando de menú de la versión 2.0 al activar un servidor OLE, no se verán afectadas por los cambios. Los comandos de la versión 2.0 han sido relacionados con sus equivalentes de versiones posteriores de Microsoft Access.

## <a name="referencing-a-control-on-a-read-only-form"></a>Hacer referencia a un control en un formulario de sólo lectura

En Microsoft Access 2002 o posterior, no es posible utilizar una expresión para hacer referencia al valor de un control en un formulario de sólo lectura que sea dependiente de un origen de registro en blanco. En las versiones anteriores, la expresión devolvería un valor **Null**. Antes de hacer referencia a un control en un formulario que sea de sólo lectura, debe asegurarse de que el origen del registro del formulario contiene registros.

## <a name="date-fields-and-data-entry"></a>Campos de fecha y entrada de datos

Si se indica **3/3** en un campo de tipo Fecha en una hoja de datos de un formulario o una tabla, el año actual se agrega automáticamente en Microsoft Access 2002 o posterior. Sin embargo, si se indica **3/3/** en el mismo campo, Microsoft Access devolverá un mensaje de error. Debe omitir el último delimitador de la fecha de forma que Microsoft Access pueda traducir la fecha al formato adecuado.

## <a name="buttons-created-with-the-command-button-wizard"></a>Botones creados con el Asistente para botones de comando

Si utilizó el Asistente para botones de comando en las versiones 2.0 o 7.0 de Microsoft Access para generar código que llama a otra aplicación, debe eliminar el botón y volver a crearlo usando el Asistente para botones de comando en Microsoft Access 2002 o posterior.

## <a name="form-and-report-class-modules"></a>Módulos de clase de formulario e informe

En las versiones anteriores a Microsoft Access 2002, los objetos **Form** y **Report** tenían asociados módulos de clase incluso cuando no había código detrás del objeto. En Microsoft Access 2002 o posterior, puede establecer en **False** la propiedad **HasModule** del formulario o informe. Cuando la propiedad **HasModule** se establece en **False**, el formulario o informe ocupa menos espacio en disco y se carga más rápidamente porque ya no tiene asociado un módulo de clase.

## <a name="converted-version-20-report-has-different-margins"></a>Informe de convertidos de la versión 2.0 tiene márgenes distintos
>>>>>>> master

Puede que encuentre problemas cuando intente imprimir u obtener la vista preliminar de un informe de Microsoft Access 2002 o posterior que ha sido convertido desde Microsoft Access 2.0 si el informe tiene alguno de los márgenes establecido en 0. Cuando se convierte un informe de Microsoft Access 2.0, los márgenes no se establecen en 0; por el contrario, se establecen en el margen mínimo para la impresora predeterminada. Esto evita que el informe imprima datos en una zona de la impresora que no sea de impresión.

Para resolver este problema, reduzca el ancho de columna, el espacio entre columnas o el número de columnas en el informe, de tal forma que el ancho de las columnas más el ancho de los márgenes predeterminados sea igual o menor que el ancho del papel.

<<<<<<< HEAD
## <a name="cant-use-the-format-property-to-distinguish-null-values-and-zero-length-strings"></a>No se puede usar la propiedad Formato (Format) para distinguir valores Nulos de cadenas de longitud cero

En las versiones 1. *x* y 2.0, puede usar la propiedad **Format** de un control para mostrar distintos valores para los valores **Null** y cadenas de longitud cero (""). En Microsoft Access 2002 o posterior, para distinguir entre los valores **Null** y las cadenas de longitud cero en un control de un formulario, establezca la propiedad **ControlSource** del control en una expresión que compruebe el caso del valor **Null**. Por ejemplo, para mostrar "Null" o "ZLS" en un control, establezca su propiedad **ControlSource** en la siguiente expresión:

<a name="iifisnullmycontrol-null-formatmycontrol-zls"></a>\=IIf (IsNull (\[MiControl\]), "Null", Format (\[MiControl\], "@; ZLS"))
=======
## <a name="cant-use-the-format-property-to-distinguish-null-values-and-zero-length-strings"></a>No se puede usar la propiedad Format para distinguir valores Null y cadenas de longitud cero

En las versiones 1. *x* y 2.0, puede usar la propiedad **Format** de un control para mostrar distintos valores para los valores **Null** y cadenas de longitud cero (""). En Microsoft Access 2002 o posterior, para distinguir entre los valores **Null** y las cadenas de longitud cero en un control de un formulario, establezca la propiedad **ControlSource** del control en una expresión que compruebe el caso del valor **Null**. Por ejemplo, para mostrar "Null" o "ZLS" en un control, establezca su propiedad **ControlSource** en la siguiente expresión:

`=IIf(IsNull([MyControl]), "Null", Format([MyControl], "@;ZLS"))`
>>>>>>> master

