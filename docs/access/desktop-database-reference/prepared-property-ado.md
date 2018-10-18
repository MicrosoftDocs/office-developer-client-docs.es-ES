---
<<<<<<< Título HEAD: preparado (propiedad) (ADO) TOCTitle: preparado (propiedad) (ADO) === título: preparado (propiedad, ADO) TOCTitle: preparado (propiedad, ADO)
>>>>>>> Master ms:assetid: 33becda2-faab-5000-8904-6ffd8c5805f2 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249105(v=office.15) ms:contentKeyID: ms.date 48544116: 18/09/2015 mtps_version: Office.15 f1_keywords:
- ado210.chm1231161 f1_categories:
- Office.Version=v15
---

<<<<<<< HEAD
# <a name="prepared-property-ado"></a>Prepared (propiedad, ADO)
=======
# <a name="prepared-property-ado"></a>Prepared (propiedad, ADO)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

Indica si se va a guardar una versión compilada de un comando antes de la ejecución.

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
=======
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
>>>>>>> master

Establece o devuelve un valor de tipo **Boolean** que, si se establece en **True**, indica que debe prepararse el comando.

## <a name="remarks"></a>Comentarios

Use la propiedad **Prepared** para que el proveedor guarde una versión preparada (o compilada) de la consulta especificada en la propiedad [CommandText](commandtext-property-ado.md) antes de la primera ejecución de un objeto [Command](command-object-ado.md). Esto puede ralentizar la primera ejecución de un comando, pero una vez que el proveedor lo compila, usará la versión compilada del comando para todas las ejecuciones siguientes, lo que dará lugar a una mejora del rendimiento.

Si la propiedad es **False**, el proveedor ejecutará el objeto **Command** directamente sin crear una versión compilada.

Si el proveedor no admite la preparación del comando, puede devolver un error en cuanto esta propiedad se establezca en **True**. Si no devuelve un error, simplemente omite la solicitud de preparar el comando y establece la propiedad **Prepared** en **False**.

