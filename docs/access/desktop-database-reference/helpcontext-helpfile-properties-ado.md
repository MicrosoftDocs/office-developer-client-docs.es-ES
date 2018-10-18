---
<<<<<<< Título HEAD: ContextoDeAyuda (HelpContext), las propiedades HelpFile (ADO) TOCTitle: ContextoDeAyuda (HelpContext), las propiedades HelpFile (ADO) ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: ms.date 48546194: 18/09 / 2015 mtps_version: Office.15
---

# <a name="helpcontext-helpfile-properties-ado"></a>Propiedades ContextoDeAyuda (HelpContext), HelpFile (ADO)

=== título: ContextoDeAyuda (HelpContext), HelpFile propiedades (ADO) TOCTitle: ContextoDeAyuda (HelpContext), HelpFile (ADO) propiedades ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: ms.date 48546194: 17/10/2018 mtps_version: Office.15
---

# <a name="helpcontext-helpfile-properties-ado"></a>ContextoDeAyuda (HelpContext), HelpFile propiedades (ADO)
>>>>>>> master

**Se aplica a**: Access 2013 | Office 2013

Indican el archivo de Ayuda y el tema asociados a un objeto [Error](error-object-ado.md).

<<<<<<< HEAD
## <a name="return-values"></a>Valores devueltos

  - **HelpContextID**: devuelve un identificador de contexto, como un valor de tipo **Long**, de un tema de un archivo de Ayuda.

  - **HelpFile**: devuelve un valor de tipo **String** que evalúa una ruta de acceso completa resuelta a un archivo de Ayuda.
=======
## <a name="return-values"></a>Valores devueltos

- **HelpContextID**: devuelve un identificador de contexto, como un valor de tipo **Long**, de un tema de un archivo de Ayuda.

- **HelpFile**: devuelve un valor de tipo **String** que evalúa una ruta de acceso completa resuelta a un archivo de Ayuda.
>>>>>>> master

## <a name="remarks"></a>Comentarios

Si se especifica un archivo de Ayuda en la propiedad **HelpFile**, la propiedad **ContextoDeAyuda (HelpContext)** se utiliza para mostrar automáticamente el tema de Ayuda que identifica. Si no hay ningún tema de Ayuda pertinente disponible, la propiedad **ContextoDeAyuda (HelpContext)** devuelve cero y la propiedad **HelpFile** devuelve una cadena de longitud cero ("").

